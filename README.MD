### Nixos uses Terraform for Azure virtual machine creation
<br>
[Using Microsoft base example](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-terraform?tabs=azure-cli)
<br>
<br>
<br>
Using in Nixos environment: 

1) execute *nix.shell* to load Azure and Terraform commands

az login -> go through Azure login process in the opened web browser

2) *terraform init -upgrade*

3) *terraform plan* 

4) *terraform apply* 
<br>
<br>

If VM creation was ok, local machine public key must be added to VM
.ssh/authorized_keys file. Azure seems to want RSA keys.  (dir and file protections chmod 700/600). Use Azure web UI portal to connect to the created machine via shell for this operation. Nano editor to create the file.
<br>
<br>
Log into new VM from local machine:
*ssh -v YOUR_AZURE_ACCOUNT@NEW_VM_IP_ADDRESS*
<br>
<br>
Destroy VM (to stop possible billing):

1) *terraform plan -destroy*
2) *terraform apply*
<br>
<br>
NOTE: Check finally VM status via Azure WEBUI protal, you might have to stop(and delete)
VM via the portal!!!







