---
title_tag: Deploy the Stack | Kubernetes
meta_desc: This page provides an overview of how to deploy a Kubernetes project as a Pulumi Stack.
title: Deploy stack
h1: "Pulumi & Kubernetes: Deploy stack"
weight: 5
menu:
  clouds:
    parent: kubernetes-get-started
    identifier: kubernetes-deploy-stack

aliases:
- /docs/quickstart/kubernetes/deploy-stack/
- /docs/get-started/kubernetes/deploy-stack/
---

Let's go ahead and deploy the stack:

```bash
$ pulumi up
```

This command instructs Pulumi to determine the resources needed to create the stack. First, a preview is shown of the changes that will be made:

```
Previewing update (dev):

     Type                           Name            Plan
 +   pulumi:pulumi:Stack            quickstart-dev  create
 +   └─ kubernetes:apps:Deployment  nginx           create

Resources:
    + 2 to create

Do you want to perform this update?
  yes
> no
  details
```

Choosing `yes` will create resources in Kubernetes.

```
Do you want to perform this update? yes
Updating (dev):

     Type                           Name            Status
 +   pulumi:pulumi:Stack            quickstart-dev  created
 +   └─ kubernetes:apps:Deployment  nginx           created

Outputs:
    name: "nginx-xw231xdt"

Resources:
    + 2 created

Duration: 11s
```

The name of the deployment that we exported is shown as a [stack output](/docs/concepts/stack#outputs).

{{< console-note >}}

Next, we'll make some modifications to the program.

{{< get-started-stepper >}}
