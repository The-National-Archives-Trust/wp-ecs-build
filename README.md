# wp-ecs-build

## Build and push Wordpress container to ECR

Get the ECR repository URI. eg 825668800000.dkr.ecr.eu-west-1.amazonaws.com

Run command line to build the Docker container and push it to ECR.

```bash
# Build WordPress
ECR_REPOSITORY=***.dkr.ecr.eu-west-2.amazonaws.com \
AWS_PROFILE=*** \
IMAGE_NAME=wp_main_site_tna_trust \
DOCKER_TAG=latest \
ROBOTS="User-agent: * \nDisallow: /" \
packer build wp-packer.json
```