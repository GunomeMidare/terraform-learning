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
Use one of the following methods to create a codespace that enables you to work with Terraform:
- Create a Codespace using an existing devcontainer.json file
- Create standard Terraform Codespace for a Repository from scratch

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

### Create standard Terraform Codespace for a Repository from scratch
On GitHub, navigate to the main page of the repository. Click the Code button, then click the Codespaces tab. Click `Create codespace on main`.

<img width="1190" height="613" alt="image" src="https://github.com/user-attachments/assets/c69fc880-10a9-465b-b1db-d916526380d4" />


Use the Command Palette (Ctrl + Shift + P) or F1) and select `Codespaces: Add Dev Container Configuration Files`.
  
<img width="1446" height="158" alt="image" src="https://github.com/user-attachments/assets/054eea87-6dae-4068-9d41-006c01e7f254" />

Select a container configuration template such as `Ubuntu`.

> [!Note]
> When setting up a GithHub Code for Terraform , the Ubuntu template is often recommended as the base for your devlopment container because it provides a lightweight, flexible, and widely compatible Linux enviroment that aligns well with Terraform's requirements.

<img width="1473" height="315" alt="image" src="https://github.com/user-attachments/assets/ace1e76d-04f6-4ea3-b17f-60f3003aff62" />

Select a feature for Terraform such as `Terraform, tflint, and TFGrunt devcontainers`. See [Terraform, tflint, and TFGrunt (terraform)](https://github.com/devcontainers/features/tree/main/src/terraform) for more information.

Use the Command Palette (Ctrl + Shift + P) or F1) and select `Rebuild Container`. Verify that you can use Terraform now using for example the command:

```terraform
terraform version
```

<img width="1109" height="272" alt="image" src="https://github.com/user-attachments/assets/c35ae32b-b151-4ac6-9467-265fd3a58f70" />

## Start the SAP BTP Terraform Training 🛠️
Use the folloing link to start the training for Gettting started with Terraform on SAP BTP:
- [Getting Started with Terraform on SAP BTP](https://learning.sap.com/courses/getting-started-with-terraform-on-sap-btp)
