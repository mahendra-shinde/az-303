1.  Login with `Login-AzAccount` 

2.  Visit the URL mentioned in Output of previous command and then copy the SECRET CODE

3.  Login with your Azure Credentials

4.  Now Back to Powershell terminal.

5.  Create a resource group and then VALIDATE my template

    ```
    $ New-AzResourceGroup -Name TestGroup -Location Southeastasia
    $ Test-AzResourceGroupDeployment -TemplateFile .\azuredeploy.json -TemplateParameterFile .\azuredeploy.parameters.json
    ```

6.  Deploy the Template

    ```
    $ New-AzResourceGroupDeployment -TemplateFile .\azuredeploy.json -TemplateParameterFile .\azuredeploy.parameters.json -ResourceGroupName testgroup -Name deploy1
    ```

7.  Check the deployment using Azure Portal.

8.  Remove Resource group

    ```
    $ Remove-AzResourceGroup -Name testgroup -confirm
    ```