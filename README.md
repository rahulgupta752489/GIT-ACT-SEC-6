# GitHub Actions Notes

## Environment Variables (env)

- Store dynamic values (e.g., database name)
- May be different between workflows
- Can be defined at:
  - Workflow level
  - Job level
  - Step level
- Used in workflow and application code
- Access using `env`

Example:

```yaml
env:
  DB_NAME: database-demo
```

---

## Secrets

- Store sensitive values
- Examples:
  - Passwords
  - API Keys
  - Database Credentials
- Can be stored at:
  - Repository level
  - Environment level
- Access using `secrets`

Example:

```yaml
${{ secrets.MONGODB_PASSWORD }}
```

---

## GitHub Actions Environments

- Jobs can use different environments

Example:

```text
testing
staging
production
```

- Can add protection rules
- Can store environment-specific secrets

Example:

```yaml
environment: testing
```

---

## Quick Memory Trick

```text
env         = Configuration

secrets     = Sensitive Data

environment = Testing / Staging / Production
```
