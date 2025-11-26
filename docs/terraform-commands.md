# Frequently Used Terraform Commands

## Goal 🎯

Document frequently used Terraform commands.

## References 📝
- []()

#### Terraform FMT 🛠️
Teh `terraform fmt` command formats Terraform configuration file contents so that it matches the canonical format and style.

```Bash
terraform fmt
```

#### Terraform Validate 🛠️
The `terraform validate` command validates the configuration files in a directory. It does not validate remote services, such as remote state or provider APIs.

```Bash
terraform validate
```

#### Terraform Plan 🛠️
The `terraform plan` command creates an execution plan, which lets you preview the changes that Terraform plans to make to your infrastructure.

```bash
terraform plan -out=<name>.out
```


#### Terraform Apply 🛠️
The terraform `apply` command executes the actions proposed in a Terraform plan.

```bash
terraform apply "<name>.out"
```

#### Terraform State List 🛠️
The `terraform state list` command lists resources within a Terraform state.

```bash
terraform state list
```


#### Terraform Destroy 🛠️
The 'terraform destroy' command deprovisions all objects managed by a Terraform configuration.

```bash
terraform destroy
```
