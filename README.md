# Azure Pipelines Operator
The Azure Pipelines Operator is an open source project designed, developed and maintained by the Devops Team at **Sela Group**.

---
# **NOTE: THIS PROJECT IS CURRENTLY IN DEVELOPMENT**
---

## Description

The Azure Pipelines Operator will allow you to configure a full and scalable build infrastructure in kubernetes by creating on-demand build agents by request. 


## How It Works

After installing the operator and configuring the credentials secret (Personal Access Token), the azure-pipelines-controller will be able to communicate and track the build queues.

<kbd>
  <img src="/doc/images/general-diagram.png" width="600">
</kbd><br/><br/>

To configure an Agent Pool to run using kubernetes jobs just create an “AgentPoolDefinition” resource as described below:

```
apiVersion: azurepipelines.sela.com/v1beta1
kind: AgentPoolDefinition
metadata:
  name: my-agent-pool
spec:
  agentPoolName: "My Agent Pool"        
  organization: "MyOrganization"
  builderImage: "leonjalfon1/builder"
  maxConcurrentBuilds: "10"
```

Then, for each build queued in the specified agent pool a kubernetes job will be created to manage the build. Once it finishes, it will be deleted.

## Architecture

TBD


## Installation

TBD


## Configuration

TBD


## Contributing

See [CONTRIBUTING](doc/CONTRIBUTING.md) for details on submitting patches and the contribution workflow.

See the project roadmap [here](doc/ROADMAP.md)


## License

Azure Pipelines Operator is under Apache 2.0 license. See the LICENSE file for details.


## Support

Azure Pipelines Operator is an open source project without official support. However, we at **Sela Group** will be happy to provide you professional services to help you with whatever you need.
