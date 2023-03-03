## cdmsWebApp Helm Charts

OUTSIDE: cdmsWebApp is a SAAS storage similar to Google Drive to store your data in remote datastore.

### Markdown

Tools:
- SpringBoot Application
- High IO minio storage
- MySQL Database to store metadata
- Google API for OAuth.

### Configure cdmsWebApp Helm repo

```markdown
helm repo add pyalive-cdmswebapp https://sarwank.github.io/HelmRepos/stable
```
### Installing the Chart
Install this chart with default values using:

```markdown
helm install my-cdmswebapp pyalive-cdmswebapp/cdmswebapp --version 0.1.0
```

For OnPrem Infra use below command: (modify the image tag as per your need & configuration) (103 tag is stable at this time)
```markdown
helm install cdmswebapp pyalive-cdmswebapp/cdmswebapp --version 0.1.0 --set  image.tag=103 --set  global.namespace=cdms -n cdms --create-namespace
```
For CD using Octopus Deploy & Helm use below command: (Set variable using octopus variables) (101 tag is stable at this time)
```markdown
helm install cdmswebapp pyalive-cdmswebapp/cdmswebapp --version 0.1.0 --set  image.tag=101 --set  global.namespace=cdms -n cdms --create-namespace
```

#### Happy Helming...
