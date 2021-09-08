## Get multiple Teams sessions on macOS

### [Install PS for Mac](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-macos?view=powershell-7.1)

### [Install Azure PS Module](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-6.4.0)
`Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

`Install-Module -Name Az -Scope CurrentUser -Repository PSGallery -Force`


### Connect to every tenant you want to set up a Teams session for and run:
`Connect-AzAccount` (login with a tenant user)
`Get-AzAccount`
Then copy the tenant ID for each one.

### Install Nativefier with NPM
`npm install nativefier`

### Create separate Teams apps for each tenant with the following command(s):
You can download this image for your custom app's icons [here](https://www.allabout365.com/wp-content/uploads/Teams.png).

`node_modules/.bin/nativefier --name "Teams - Tenant Name" --icon Teams.png "https://teams.microsoft.com/_?tenantID=[TENANT_ID]"`
