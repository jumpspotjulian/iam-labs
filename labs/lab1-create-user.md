# Lab 1: Create an Azure AD User and Assign Reader Role

## Objective
Create a new Azure AD user and assign them the built-in Reader role for a resource group using Azure CLI.

---

## Steps

1. **Login to Azure CLI**

```bash
az login

2. **Create a user**

az ad user create --display-name "Test User" --user-principal-name testuser@yourdomain.com --password "StrongPassword123!"

3. **Assign a role**

az role assignment create --assignee testuser@yourdomain.com --role Reader --scope /subscriptions/{subscription-id}/resourceGroups/{resource-group}

Notes
Replace {subscription-id} and {resource-group} with your actual values

Passwords used are for demo purposes only — use secure secrets in production

References
Azure CLI Docs - az add user

Role Assignment
