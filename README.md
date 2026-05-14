# Maven GitHub Actions CI Pipeline

A Java Maven project with a GitHub Actions CI pipeline that builds, tests, and uploads the artifact on every push or pull request to `main`.

---

## CI Pipeline

**Trigger:** Push or pull request to `main`

| Step               | Description                                      |
|--------------------|--------------------------------------------------|
| Checkout Code      | Clones the repository                            |
| Setup Java         | Installs Java 18 (Temurin distribution)          |
| Cache Maven        | Caches `~/.m2` to speed up subsequent builds     |
| Build & Test       | Runs `mvn clean install`                         |
| Upload Artifact    | Uploads the built `.jar` as a workflow artifact  |

---

## Run Locally

```bash
# Build and test
mvn clean install

# Skip tests
mvn clean install -DskipTests
```

---

## Tech Stack

- Java 18
- Apache Maven
- GitHub Actions

---
