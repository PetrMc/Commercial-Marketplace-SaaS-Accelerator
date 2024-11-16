wget https://dotnet.microsoft.com/download/dotnet/scripts/v1/dotnet-install.sh; `
chmod +x dotnet-install.sh; `
./dotnet-install.sh; `
$ENV:PATH="$HOME/.dotnet:$ENV:PATH"; `
dotnet tool install --global dotnet-ef; `
git clone https://github.com/PetrMc/Commercial-Marketplace-SaaS-Accelerator.git -b updated-site-1115 --depth 1; `
cd ./Commercial-Marketplace-SaaS-Accelerator/deployment; `
.\Deploy.ps1 `
 -WebAppNamePrefix "SOLO-SITE" `
 -ResourceGroupForDeployment "SOLO-TRANSACTABLE-OFFER-RG" `
 -PublisherAdminUsers "petr.mcallister@solo.io,petr@solo.io" `
 -Location "East US" 

```output

 ✅ If the intallation completed without error complete the folllowing checklist:
   🔵 Add The following URL in PartnerCenter SaaS Technical Configuration
      ➡️ Landing Page section:       https://SOLO-SITE-portal.azurewebsites.net/
      ➡️ Connection Webhook section: https://SOLO-SITE-portal.azurewebsites.net/api/AzureWebhook
      ➡️ Tenant ID:                  5e7d8166-7876-4755-a1a4-b476d4a344f6
      ➡️ AAD Application ID section: 303020a5-b0bc-4a1c-8955-1a78777675f6
Deployment Complete in 17m:28s
DO NOT CLOSE THIS SCREEN.  Please make sure you copy or perform the actions above before closing.
```

``` powershell
wget https://dotnet.microsoft.com/download/dotnet/scripts/v1/dotnet-install.sh; `
chmod +x dotnet-install.sh; `
./dotnet-install.sh; `
$ENV:PATH="$HOME/.dotnet:$ENV:PATH"; `
dotnet tool install --global dotnet-ef; `
git clone https://github.com/PetrMc/Commercial-Marketplace-SaaS-Accelerator.git -b updated-site-1115 --depth 1; `
cd ./Commercial-Marketplace-SaaS-Accelerator/deployment; `
.\Upgrade.ps1 `
 -WebAppNamePrefix "SOLO-SITE" `
 -ResourceGroupForDeployment "SOLO-TRANSACTABLE-OFFER-RG" `
 ```