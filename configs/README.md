# Docker Compose
## AWS
```shell
docker compose -f ~/workspace/operations/docker-compose.yml run --rm aws-cli configure sso
docker compose -f ~/workspace/operations/docker-compose.yml run --rm aws-cli sso login --profile profile_name
```

## Google Cloud
```shell
docker compose -f ~/workspace/operations/docker-compose.yml run --rm gcloud-cli init
```shell

## Terraform
### AWS
```shell
TERRAFORM_VERSION=1.3.6 AWS_PROFILE=profile_name docker compose -f ~/workspace/operations/docker-compose.yml run --rm terraform init
```

### Google Cloud
```shell
TERRAFORM_VERSION=1.3.6 GCLOUD_PROJECT=project_id docker compose -f ~/workspace/operations/docker-compose.yml run --rm terraform init
```

### Renovate
```shell
docker compose -f ~/workspace/operations/docker-compose.yml run --rm renovate --dry-run=true --require-config=ignored org/repo
```
