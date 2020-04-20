# Contributing

## Before Start Developing
---

The azure-pipelines-operator uses the go operator-sdk which is a component of the Operator Framework, for more details see: https://github.com/operator-framework/operator-sdk

A recommended way to get started with kubernetes operators developement is perform the following tutorial: https://github.com/leonjalfon1/k8s-operator-dev-demo


## Prerequisites
---

 - git
 - go version v1.13+
 - docker version 17.03+
 - kubectl version v1.12.0+
 - Access to a Kubernetes v1.12.0+ cluster
 - Operator SDK CLI ([installation guide](https://github.com/operator-framework/operator-sdk/blob/master/doc/user/install-operator-sdk.md))


## Setup Your Dev Environment
---

Configure a working Go environment by run

```
mkdir -p $GOPATH/src/leonjalfon1
cd $GOPATH/src/leonjalfon1
export GO111MODULE=on
git clone https://github.com/leonjalfon1/azure-pipelines-operator.git
```

Install dependencies

```
cd azure-pipelines-operator
go mod tidy
```


## Project Roadmap
---

You can find the project roadmap [here](doc/ROADMAP.md)


## Open Bugs
---

If any part of the project has bugs or documentation mistakes, please let us know by [opening an issue][azure-pipelines-operator-issue]. We treat bugs and mistakes very seriously and believe no issue is too small. Before creating a bug report, please check that an issue reporting the same problem does not already exist.

To make the bug report accurate and easy to understand, please try to create bug reports that are:

 - Specific. Include as much details as possible: which version, what environment, what configuration, etc.

 - Reproducible. Include the steps to reproduce the problem. We understand some issues might be hard to reproduce, please include the steps that might lead to the problem.

 - Isolated. Please try to isolate and reproduce the bug with minimum dependencies. It would significantly slow down the speed to fix a bug if too many dependencies are involved in a bug report. Debugging external systems that rely on operator-sdk is out of scope, but we are happy to provide guidance in the right direction or help with using operator-sdk itself.

 - Unique. Do not duplicate existing bug report.

 - Scoped. One bug per report. Do not follow up with another bug inside one report.

It may be worthwhile to read [Elika Etemad’s article on filing good bug reports][filing-good-bugs] before creating a bug report.

We might ask for further information to locate a bug. A duplicated bug report will be closed.


## Feature Requests
---

Good ideas are always welcome, if you have any, please let us know by [opening an issue][azure-pipelines-operator-issue]


## Contribution flow
---

This is a rough outline of what a contributor's workflow looks like:

 - Fork the repository
 - Create a topic branch from where to base the contribution. This is usually master.
 - Make commits of logical units.
 - Make sure commit messages are are informative and clear.
 - Push changes in a topic branch to a personal fork of the repository.
 - Submit a pull request to leonjalfon1/azure-pipelines-operator.
 - The PR must be reviewed by the repository mantainer before being approved.

Thanks for contributing!


[filing-good-bugs]: http://fantasai.inkedblade.net/style/talks/filing-good-bugs/
[azure-pipelines-operator-issue]: https://github.com/leonjalfon1/azure-pipelines-operator/issues/new