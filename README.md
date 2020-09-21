[![Board Status](https://dev.azure.com/surao/979dae51-0fd4-41bb-8992-a0f4d653df39/ca26a3b8-5507-4221-95e6-93591fea985c/_apis/work/boardbadge/5b76fbce-125d-4217-b9cd-8fefd94e15da)](https://dev.azure.com/surao/979dae51-0fd4-41bb-8992-a0f4d653df39/_boards/board/t/ca26a3b8-5507-4221-95e6-93591fea985c/Microsoft.FeatureCategory)
---
page_type: sample
languages:
- csharp
- sql
products:
- azure
description: "This repo contains the code for the provisioning of the resources necessary to execute a DevOps openhack event."
---

# DevOps Openhack Proctor Repository

This repo contains the code for the provisioning of the resources necessary to execute a DevOps openhack event.  The relevant code individual teams use (i.e. the APIs) to complete their challenges can be found in the [DevOps Openhack Team repository](https://github.com/Azure-Samples/openhack-devops-team/).

## Components

The components are organized by folders which contain the following:

* **leaderboard** - visualizes the uptime for the teams' APIs and contains an Azure Functions API which connects to CosmosDB, Sentinel (pods to query the APIs and report status), and a web front end.
* **provision-proctor** - code to support the provisioning of a complete proctor environment (1 needed per event).
* **provision-team** - code to support the provisioning of a complete team environment.
* **provision-vm** - automates the provisioning of an Ubuntu 16.04 VM used as the foundation for provisioning the team and proctor environments.
* **simulator** - simulates traffic to the SQL database the APIs use for every team's environment.

Go to the root of these folders to see a readme with deeper information on each component.

## Getting Started

### Prerequisites

The first step is to create a virtual machine which has the necessary software installed required to provision the teams and proctor environments.  In order to create the VM, only the following needs to be installed

* Azure PowerShell
* An Azure Subscription

### High-Level Installation Flow

 [Deploy a team environment](./provision-vm) using the Azure Resource Manager template.

## Resources

For troubleshooting or answers to common questions, please [read the FAQ](FAQ.md).
