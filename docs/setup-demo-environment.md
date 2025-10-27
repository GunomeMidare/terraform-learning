# Create a Demo Setup for SAP BTP and Terraform 

## Goal 🎯

The goal of this file is to document the setup of deomo setup for using Terraform for SAP BTP.

## References 📝
- [SAP BTP Trail Environment](https://account.hanatrial.ondemand.com/trial/#/home/trial)
- [Getting Started with Terraform on SAP BTP](https://learning.sap.com/courses/getting-started-with-terraform-on-sap-btp)

## Prerequisites 🎯
- You have a Github Account
- You have an SAP SUSER

## Create SAP BTP Trial Account 🛠️
**1.** Navigate to the following link:

  - [SAP BTP Trail Environment](https://account.hanatrial.ondemand.com/trial/#/home/trial)

**2.** Create a SAP BTP Trial Account.


## Create Github Repository & Codespace🛠️
### Create a Codespace using an existing devcontainer.json file
1. Create a file named `devcontainer.json` in a directory named `.devcontainer`.

	<img width="990" height="354" alt="image" src="https://github.com/user-attachments/assets/aab34d9f-0d92-4b26-816c-3e3a928120f6" />
   
2. Enter the following code and commit.

```
// For format details, see https://aka.ms/devcontainer.json. For config options, see the
// README at: https://github.com/devcontainers/templates/tree/main/src/ubuntu
{
	"name": "Ubuntu",
	// Or use a Dockerfile or Docker Compose file. More info: https://containers.dev/guide/dockerfile
	"image": "mcr.microsoft.com/devcontainers/base:noble",
	"features": {
		"ghcr.io/devcontainers/features/terraform:1": {
			"installTerraformDocs": true,
			"version": "latest",
			"tflint": "latest",
			"terragrunt": "latest"
		}
	},
	"customizations": {
		"vscode": {
			"extensions": [
				"nopjmp.fairyfloss"
			],
			"settings": {
				"workbench.colorTheme": "fairyfloss"   
			}
		}
	}

	// Features to add to the dev container. More info: https://containers.dev/features.
	// "features": {},

	// Use 'forwardPorts' to make a list of ports inside the container available locally.
	// "forwardPorts": [],

	// Use 'postCreateCommand' to run commands after the container is created.
	// "postCreateCommand": "uname -a",

	// Configure tool-specific properties.
	// "customizations": {},

	// Uncomment to connect as root instead. More info: https://aka.ms/dev-containers-non-root.
	// "remoteUser": "root"
}
```
3. Start your codespace.
