## cdmsWebApp Helm Chart

cdmsWebApp is a SAAS storage similar to Google Drive to store your data in remote datastore.

### Markdown

Tools:
- SpringBoot Application
- High IO minio storage
- MySQL Database to store metadata
- Google API for OAuth.

### Configure cdmsWebApp Helm repo

```markdown
helm repo add cdmswebapp https://sarwank.github.io/Helm3/stable
```
### Installing the Chart
Install this chart using:

```markdown
helm install my-cdmswebapp cdmswebapp/cdmswebapp
```

For OnPrem Infra use below command: (modify the image tag as per your need & configuration) (80 tag is stable at this time)
```markdown
helm upgrade --install cdmswebapp cdmsWebApp-x.1.0 --set  image.tag=80 --set  global.namespace=cdms -n cdms --create-namespace
```
For CD using Octopus Deploy & Helm use below command: (Set variable using octopus variables) (93 tag is stable at this time)
```markdown
helm upgrade --install cdmswebapp cdmsWebApp-x.1.0 --set  image.tag=93--set  global.namespace=cdms -n cdms --create-namespace
```

#### Happy Helming
