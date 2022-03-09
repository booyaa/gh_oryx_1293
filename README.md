# repo for Oryx team to reproduce the problem

## setup

- App Service Plan: P1v2
- OS : Linux
- Stack: PHP
- Major Version: PHP 7.4
- Deploy slot called "maintenance"

## usage

```sh
zip -r upload.zip index.html .htaccess
app_rg_name=CHANGE ME
app_name=CHANGE ME
az webapp deploy --type zip --resource-group "$app_rg_name" --name "$app_name" --slot maintenance --src-path upload.zip
```
