# Flow & PowerApps Migrator

Have you ever tried moving PowerApps or MS Flow from one Office 365 tenant to another? If you have SharePoint as a data source - then the only official way is to remove all such data sources and add them back. These PowerShell scripts 


## 1. Install [PnP PowerShell](https://github.com/SharePoint/PnP-PowerShell) prerequisites
Run the script below:

`Install-Module SharePointPnPPowerShellOnline` |

## 2. Navigate to the FlowPowerAppsMigrator folder

![](2018-07-25-20-53-52.png)


## 3. Place all your exported MS Flow and PowerApps files in the src folder
![](2018-07-25-20-57-29.png)

## 4. Run RunAllSripts.ps1 form PowerShell
The scripts will iterate through all zip files inside the \src directory and convert them to be compatible with the new Office 365 tenant.
- `powershell`
- `cd C:\FlowPowerAppsMigrator`
- `.\RunAllSripts.ps1`

![](2018-07-25-21-00-48.png)

Example:
![](2018-07-25-21-08-30.png)

## 5. Navigae to the \dist folder and collect converted MS Flow and PowerApps packages

![](2018-07-25-21-11-04.png)

## 6. Done! Now go ahead and import your MS Flow and PowerApps packages to the destination tenant
All SharePoint Datasources should be converted to point to the new tenant that you chose. 

![](2018-07-25-21-14-55.png)