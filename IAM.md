# 🔐 IAM – Identity and Access Management (AWS)

IAM (Identity and Access Management) is a foundational service in AWS that allows you to **securely control access** to AWS services and resources.

---

## 🧾 What is IAM?

IAM enables you to:
- Manage **users**, **groups**, and **permissions**
- Define **who** can access **what**, and **how**

It’s used to implement the **principle of least privilege**, meaning users get **only the access they need** — nothing more.

---

## 🧑‍🤝‍🧑 IAM Components

| Component   | Description |
|-------------|-------------|
| **User**     | An identity for a person or application that interacts with AWS |
| **Group**    | A collection of users with identical permissions |
| **Policy**   | A JSON document that defines permissions |
| **Role**     | An identity that can be assumed by trusted entities (like services or users from another account) |
| **Identity Provider (IdP)** | External authentication source (e.g., Google, AD, etc.) |

---

## 🗂️ IAM Policies

- **Written in JSON**
- Attached to **users**, **groups**, or **roles**
- Define **Allow** or **Deny** actions on specific resources

### 🧾 Example Policy (Read access to S3):

```json
{
  "Version": "YYYY-MM-DD",
  "Statement": [{
    "Effect": "Allow",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::mybucket/*"
  }]
}
