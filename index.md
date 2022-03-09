# Example Azure DevOps Pipeline Definition to use Power Platform CLI
1. NuGet tool Installer Task
2. NuGet Command 
   - Commanmd
     - Custom
   - Custom Command and Arguments
     - install Microsoft.PowerApps.CLI -OutputDirectory pac
3. PowerShell Task
   - Type
     - Inline
   - Script
<pre><code class="language-powershell">##PowerShell SCRIPT
##$(connectionUrl) - String Stored as Pipeline variable. e.g. https://organisation.crm6.dynamics.com
##$(applicationId) - environment spn - Secure String Stored as Pipeline variable or linked KeyVault
##$(clientSecret) - spn secret - Secure String Stored as Pipeline variable or linked KeyVault
##$(environmentName) environment - String Stored as Pipeline variable
##$(portalId) - GUID representing the Website in PowerApps Portals - found in Portal Management App

$pacFolder = Get-ChildItem "pac" | Where-Object {$_.Name -match "Microsoft.PowerApps.CLI."}
$env:PATH = $env:PATH + ";" + $pacFolder.FullName + "\tools"

## Execute your commands using PowerPlatform CLI.
## authenticate to your environment
pac auth create -u $(connectionUrl) -n $(environmentName) -id $(applicationId) -cs $(clientSecret)

## execute portal download directly to the staging directory portal path to be used later
pac paportal  download -p "$(Build.ArtifactStagingDirectory)\portal" -id $(portalId)
</code></pre>
4. Publish Artifact
   - Accept Defaults unless different download directory is specified in PowerShell script


The YAML is as per above in the class editor
<pre><code>pool:
  name: Azure Pipelines
variables:
  connectionUrl: ''
  applicationId: ''
  clientSecret: ''
  portalId: ''
  environmentName: ''

steps:
- task: NuGetToolInstaller@1
  displayName: 'Use NuGet'

- task: NuGetCommand@2
  displayName: 'Install PowerPlatform CLI'
  inputs:
    command: custom
    arguments: 'install Microsoft.PowerApps.CLI -OutputDirectory pac'

- powershell: |
   $pacFolder = Get-ChildItem "pac" | Where-Object {$_.Name -match "Microsoft.PowerApps.CLI."}
   $env:PATH = $env:PATH + ";" + $pacFolder.FullName + "\tools"
   
   ## Execute your commands using PowerPlatform CLI.
   ## authenticate to your environment
   pac auth create -u $(connectionUrl) -n $(environmentName) -id $(applicationId) -cs $(clientSecret)
   
   ## execute portal download directly to the staging directory portal path to be used later
   pac paportal  download -p "$(Build.ArtifactStagingDirectory)\portal" -id $(portalId)
  displayName: 'Download Portal Package'

- task: PublishBuildArtifacts@1
  displayName: 'Publish Artifact: drop'
</code></pre>
