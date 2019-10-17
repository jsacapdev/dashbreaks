# Dash Breaks This

`az group create -n dash-breaks-this -l westeurope --debug`

`az storage account create -g dash-breaks-this -n dashbreaksthis -l westeurope --sku Standard_LRS --debug`

`az functionapp plan create -g dash-breaks-this -n dash-breaks-this-plan --sku S1 --debug`

`az functionapp create -g dash-breaks-this -n dash-breaks-this --storage-account dashbreaksthis --plan dash-breaks-this-plan --debug`

`dotnet publish -c Release -o d:/api`

`az functionapp deployment source config-zip -g dash-breaks-this -n dash-breaks-this --src d:/api/api.zip --debug`
