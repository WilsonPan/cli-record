# Azure CLI

## Auth

- azure login

```bash
az login                                        # open brewser to login
az login -u <username> -p <password>            # usename and password login
az login --tenant <tenant>                      # use different tenant login
```

- switch tenant
  
```bash
az account list --output table                  # list accounts as table
az account set --subscription "Wilson"          # switch others subscriptions    
```

- virtual machines

```bash
az vm list --output table                       # list virtual machines as table 
az vm list --output table -d                    # list virtual machines details as table
az vm list -g ResourceGroup --output table      # list virtual machines of ResourceGroup as table
```
