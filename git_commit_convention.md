# Git Commit Message Types — Conventional Commits

> A quick reference for writing consistent and meaningful commit messages.

---

## Type Table

| Type | Emoji | When to Use | Example |
|---|---|---|---|
| `feat` | ✨ | Introducing a new feature | `feat(auth): add OAuth2 login` |
| `fix` | 🐛 | Fixing a bug | `fix(api): handle null response from DynamoDB` |
| `docs` | 📝 | Documentation changes only | `docs(readme): add ECS architecture diagram` |
| `style` | 💄 | Formatting, whitespace, missing semicolons (no logic change) | `style(lambda): reformat handler indentation` |
| `refactor` | ♻️ | Code restructure without adding features or fixing bugs | `refactor(sqs): simplify message retry logic` |
| `test` | ✅ | Adding or updating tests | `test(api): add unit tests for token validation` |
| `chore` | 🔧 | Build process, config, dependency updates | `chore(deps): upgrade AWS SDK to v3` |
| `perf` | ⚡️ | Performance improvements | `perf(cache): add ElastiCache for session lookup` |
| `ci` | 👷 | CI/CD pipeline changes | `ci(github-actions): add deploy workflow to ECS` |
| `build` | 📦 | Changes affecting build system or external dependencies | `build(docker): update base image to node 20` |
| `revert` | ⏪ | Reverting a previous commit | `revert: revert feat(auth): add OAuth2 login` |

---

## Full Commit Structure

```
<type>(<scope>): <short summary>

[optional body — explain WHY, not WHAT]

[optional footer — e.g. BREAKING CHANGE, issue refs]
```

---

## Golden Rules

1. ✅ Use **imperative mood** — `add feature` not `added feature`
2. ✅ Keep subject **under 50 characters**
3. ✅ **No period** at the end of the subject line
4. ✅ Separate subject and body with a **blank line**
5. ✅ Explain **why** in the body, not what (the diff already shows what)

---

## Real-World Examples for AWS Repos

```bash
feat(ecs): add auto-scaling policy for task count
fix(vpc): correct private subnet CIDR block overlap
docs(patterns): add Saga pattern with Step Functions
refactor(lambda): extract DynamoDB client to shared layer
chore(cdk): update constructs library to v2.80.0
perf(apigw): enable response caching for GET endpoints
ci(github-actions): add ECR push step to deploy pipeline
test(sqs): add integration test for dead-letter queue
```

---

## Scope Examples for AWS Architecture Repo

| Scope | Meaning |
|---|---|
| `ecs` | ECS service or task definition changes |
| `eks` | Kubernetes / EKS related |
| `lambda` | Lambda function changes |
| `vpc` | Networking / VPC config |
| `apigw` | API Gateway |
| `sqs` / `sns` | Messaging services |
| `rds` / `dynamo` | Database changes |
| `iam` | IAM roles or policies |
| `cdk` / `cfn` | Infrastructure as Code |
| `cicd` | Pipeline configuration |
| `patterns` | Architecture pattern docs |

---

> 📎 Reference: [conventionalcommits.org](https://www.conventionalcommits.org/)
