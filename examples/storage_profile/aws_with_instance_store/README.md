# storage_profile example for AWS with instance store device type

This is an example on how to create an AWS Storage Profile with instance store device type. 

## Getting Started

There are variables which need to be added to terraform.tfvars. The first are for connecting to the vRealize Automation (vRA) endpoint. The others are names of cloud_account, and region that already setup in vRA.

Following is the full list of variables used in this example.

* `url` - The URL for the vRealize Automation (vRA) endpoint
* `refresh_token` - The refresh token for the vRA account
* `cloud_account` - The name of the AWS cloud account added in vRA
* `region` - The region within the AWS cloud account

To facilitate adding these variables, a sample tfvars file can be copied first:
```shell
cp terraform.tfvars.sample terraform.tfvars
``` 

Follow these examples for setting up specific cloud accounts:

* Setup [cloud\_account\_aws](../../cloud_account_aws/README.md)
* Setup [cloud\_account\_azure](../../cloud_account_azure/README.md)
* Setup [cloud\_account\_gcp](../../cloud_account_gcp/README.md)
* Setup [cloud\_account\_vmc](../../cloud_account_vmc/README.md)
* Setup [cloud\_account\_vsphere](../../cloud_account_vsphere/README.md)

Once the information is added to `terraform.tfvars`, the Storage Profile can be created via:

```shell
terraform init
terraform apply
```
