# Creating the Subaccount Domain Value

## Goal 🎯

The goal of this file is to document the setup of the Subaccount Domain value for the resource: 

## References 📝
- [`random_uuid`](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/uuid)
- [btp_subaccount (Resource)](https://registry.terraform.io/providers/SAP/btp/latest/docs/resources/subaccount)
- 

## Creating the Subaccount Domain Attribute of the Resource:  🛠️

The subdomain will become part of the URL for accessing applications that you subscribe to from this subaccount. The subdomain can contain only letters, digits, and hyphens (not allowed at the beginning or at the end), and must be unique across all subaccounts in the same region.

<img width="1349" height="638" alt="image" src="https://github.com/user-attachments/assets/6fc06226-d0a2-4cdb-ba36-94a797c203f1" />





To ensure that the Subaccount domain is unique, we also must add a UUID to it. This ensures that it is unique and we do not run into any naming conflicts on SAP BTP.
Terraform offers a resource for the creation of UUIDs out of the box. It is called [`random_uuid`](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/uuid).

You can add this new resource in the `main.tf` file at the top:

```terraform
resource "random_uuid" "uuid" {}
```
