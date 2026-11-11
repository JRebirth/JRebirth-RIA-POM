# Publish `org.jrebirth:ria` to Maven Central

Same pattern as [JRebirth-Organization-POM](https://github.com/JRebirth/JRebirth-Organization-POM/blob/master/README-MAVEN-CENTRAL.md).

## Secrets (repo Actions)

`CENTRAL_USERNAME`, `CENTRAL_TOKEN`, `GPG_PRIVATE_KEY`, `GPG_PASSPHRASE`

Public signing key must be on https://keys.openpgp.org (confirm email).

## Local

```bash
mvn -f org.jrebirth.ria/pom.xml -B -Pdeploy-central,-OJO clean deploy
```

## GitHub Actions

- Tag: `ria-4.0.0`
- Or workflow_dispatch with version `4.0.0`

Profile: `-Pdeploy-central,-OJO` (disables default OJO Artifactory URLs).
