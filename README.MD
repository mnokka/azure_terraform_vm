### Nixos uses Terraform for Azure virtual machine creation
<br>
[Using Microsoft base example](https://learn.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-terraform?tabs=azure-cli)
<br>
<br>
<br>
Using in Nixos environment: 

1) execute *nix.shell* to load Azure and Terrform commands

2) terraform init -upgrade

3) terraform plan 

4) terraform apply 
<br>
<br>

If VM creation was ok, local machine public key must be added to VM
.ssh/know_hosts file. Azure seems to want RSA keys.  (dir and file protections chmod 700/600). Use Azure web UI portal to connect to the created machine via shell for this operation
<br>
<br>
Log into new VM from local machine:
*ssh -v YOUR_AZURE_ACCOUNT@NEW_VM_IP_ADDRESS*
<br>
<br>
Destroy VM (to stop possible billing):

1) terraform plan -destroy
2) terraform apply









