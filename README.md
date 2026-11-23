# mulesoft-error-handler-plugin
Standardized MuleSoft error handling framework with reusable strategies and mappings.

## Releasing
A merge into `main` releases the version of the POM: the pipeline makes the tag `vX.Y.Z`, publishes `X.Y.Z` to the org's Exchange and moves `main` to the next SNAPSHOT. For a minor or a major, change the version in the pull request (for example, to `1.2.0-SNAPSHOT`).

## Testing a SNAPSHOT in an API before the merge
Exchange takes the asset only under the org's ID, which git does not hold. Publish from a copy of the repository, with your settings.xml configured for Exchange, and commit nothing:

```
cp -R . /tmp/mulesoft-error-handler-plugin && cd /tmp/mulesoft-error-handler-plugin
sed -i.bak 's#<groupId>com.brunosouzas.mulesoft</groupId>#<groupId><YOUR_ORG_ID></groupId>#' pom.xml
mvn clean org.mule.tools.maven:exchange-mule-maven-plugin:0.0.23:exchange-pre-deploy deploy org.mule.tools.maven:exchange-mule-maven-plugin:0.0.23:exchange-deploy
```

A consumer references the asset by the org's ID: `<groupId><YOUR_ORG_ID></groupId>`.
