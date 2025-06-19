# VM Reader Lite Custom Role Lab

This lab demonstrates how to create a custom Azure Role with limited VM read access.

## Purpose

The role `VM Reader Lite` grants read-only access to virtual machines across the assigned subscription scope.

## Role Definition

```json
{
  "name": "VM Reader Lite",
  "isCustom": true,
  "description": "Can view virtual machines only",
  "actions": [
    "Microsoft.Compute/virtualMachines/read"
  ],
  "notActions": [],
  "assignableScopes": [
    "/subscriptions/<your-subscription-id>"
  ]
}

## Deployment Command

az role definition create --role-definition ./vm-reader-lite.json

## Output Example

{
  "roleName": "VM Reader Lite",
  "roleType": "CustomRole",
  "permissions": [
    {
      "actions": ["Microsoft.Compute/virtualMachines/read"]
    }
  ],
  ...
}

