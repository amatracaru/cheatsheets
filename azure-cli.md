---
title: Azure CLI
category: Devops
layout: 2017/sheet
updated: 2018-01-28
intro: Cheatsheet for *Azure CLI 2.0*
---

### Login

```bash
az login # interactive login
```

### Find commands

```bash
az find -q vm # search for commands containing `vm`
```

### Interactive mode

```bash
az interactive
```

## Resource Groups

### Create

```bash
az group create
  --location, -l
  --name, -n
```
### Retrieve

```bash
az group list          # show all resource groups
az group show --name   # get specified resource group
az group exists --nane # check if resource group exists
```

### Delete

```bash
az group delete
  --name, -n
  --no-wait
  --yes, -y  # do not prompt for confirmation
```

[All Resource Group Commands](https://docs.microsoft.com/en-us/cli/azure/group?view=azure-cli-latest#Commands)

## Virtual Machines

### Create

```bash
az vm create 
  --name, -n            # vm name
  --resource-group, -g  # resource group name
  [--image]             # vm image name; `az vm image list` for options
  [--admin-username]     
  [--admin-password]     
  [--size]              # vm size; `az vm list-sizes` for options
  [--no-wait]           # don't wait for operation to finish
```

[All VM Commands](https://docs.microsoft.com/en-us/cli/azure/vm?view=azure-cli-latest)

## Also see

* [Azure CLI Docs](https://docs.microsoft.com/en-us/cli/azure/overview?view=azure-cli-latest)


