# CI/CD Pipeline and Workflow

## Gitlab

### Initializing a Gitlab repository

After create a Gitlab repo, it needs to be added as a remote repository in a local project directory.

In the directory where the code will be set:

```bash
git init
git add .
git commit -am "Mensagem qualquer"
# The Gitlab address and port should be present in the the Docker Compose environment variable "external_url".
# Like: external_url 'http://localhost:40280'
git remote add origin http://<Gitlab address>:<Gitlab port>/<Username of the account that created the Gitlab repo>/<repo name>.git
# Like:
git remote add origin http://localhost:40280/victoralm/teste_01.git
```
