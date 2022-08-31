# Octopus Builder
This repo was populated by the [Octopus Builder](https://github.com/OctopusSamples/content-team-apps) tool. The directory structure is shown below:

* `.github/workflows`: GitHub Action Workflows that populate a cloud Octopus instance, build and deploy the sample code, and initiate a deployment in Octopus.
* `github`: [Composable GitHub Actions](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action) that are called by the workflow files.
* `terraform`: Terraform templates used to create cloud resources and populate the Octopus cloud instance with the [Octopus Terraform provider](https://registry.terraform.io/providers/OctopusDeployLabs/octopusdeploy/latest/docs).
* `java`: The sample Java application.
* `js`: The sample JavaScript application.
* `golang`: The sample Go application.
## Network Diagram
![Network Diagram](/images/diagram.png)
## Rerunning Octopus Builder
If you have run the Octopus Builder for a second time, the files are placed in the `app-builder-update` branch.
The workflow files are configured to not run from this branch, meaning any changes you have made in the main branch will not be overwritten.
To replace the `main` branch with the `app-builder-update` branch, [run the following commands](https://stackoverflow.com/a/2862938/157605):
1. `git checkout app-builder-update`
2. `git merge -s ours main`
3. `git checkout main`
4. `git merge app-builder-update`

If you would rather see what has changed since you last ran the Octopus Builder, create a regular pull request between the `app-builder-update` and `main` branches.

## Videos
### Introduction
[![Introduction](https://user-images.githubusercontent.com/160104/171066204-faa47ace-9cef-40a5-b919-5074f662c045.png)](https://oc.to/QoaFL7)
### Testing
[![Testing](https://user-images.githubusercontent.com/160104/171066350-86616af1-1b74-4c3b-b914-636e15b4f0f9.png)](https://oc.to/LdAw6T)
### Security Testing
[![Security Testing](https://user-images.githubusercontent.com/160104/171066462-15c095b4-f7b7-4a52-b2f4-1b4239c48c74.png)](https://oc.to/tOL83r)
### Feature Branching
[![Feature Branching](https://user-images.githubusercontent.com/160104/171066536-46a1480d-abe5-44da-b8b3-c69d4fc8274f.png)](https://oc.to/JgsP6z)