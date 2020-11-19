# Heroku Buildpack for Kubectl

Add the `kubectl` binary to your Heroku app.

Configuration:

* `KUBERNETES_VERSION` can specify a version of the Kubernetes CLI to install. If unset, this buildpack will use the latest version.
* `KUBECONFIG` can contain a complete Kubernetes configuration file, base64-encoded. If set, it will be deployed to your dynos on startup.

## Example

```bash
heroku buildpacks:add heroku-community/kubectl

heroku config:set KUBECONFIG_CONTENT=$(base64 configfile)
```
