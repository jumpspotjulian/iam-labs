# RBAC User Role Assignment Lab

## 🧠 Objective
Create a new user in Microsoft Entra ID and assign the **Reader** role scoped to a subscription.

---

## ⚙️ Steps Performed

1. Created a new user using Azure CLI
2. Assigned the Reader role scoped to a subscription
3. Verified role assignment in Azure Portal

---

## 🧪 Commands Used

```bash
# Create user (UPN hidden for privacy)
az ad user create \
  --display-name "Lab User" \
  --user-principal-name <UPN> \
  --password "<SecurePassword123>" \
  --force-change-password-next-login true

# Assign Reader role
az role assignment create \
  --assignee <UPN> \
  --role "Reader" \
  --scope /subscriptions/<your-subscription-id>
