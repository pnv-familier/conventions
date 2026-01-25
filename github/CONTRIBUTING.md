# 🤝 Contributing Guide

This project follows strict conventions to ensure clean collaboration and Jira traceability.

---

## 1. Jira Is Mandatory

- Every code change must be linked to **one Jira ticket**
- No ticket → no code

---

## 2. Branch Rules

### Protected Branches

- `main` → stable / release
- `dev` → development

❌ Do not commit directly to `main`

### Branch Naming

```
<type>/<JIRA-KEY>-short-description
```

**Types**

- `feature` – new functionality
- `bugfix` – bug fixes
- `chore` – refactor / cleanup
- `hotfix` – urgent fixes

**Example**

```
feature/MOB-12-chat-ui
```

---

## 3. Commit Message Format

```
<type>(<JIRA-KEY>): short description
```

**Examples**

```
feature(MOB-12): add chat screen layout
bugfix(BE-34): fix token expiration
```

Rules:

- Jira key is required
- One ticket per commit
- Keep messages short and clear

---

## 4. Pull Requests

### PR Title

```
<JIRA-KEY> - short description
```

### PR Rules

- One PR = one Jira ticket
- Target branch: `dev`
- No unrelated changes

---

## 5. Before Merging

- Code follows project architecture
- No debug or unused code
- PR is reviewed and approved

---

## Final Rule

> If your change cannot be understood in 5 minutes, it is not ready to merge.
