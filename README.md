# hbp_docker_recipe
Recipe to generate the docker container able to run automated model verification workflow

# Build the container
docker build --file ./docker-ebrains-base.def --tag docker-registry.ebrains.eu/hbp-model-validation/docker-ebrains-base .

docker run -e HBP_USER -e HBP_PASSWORD -e WORKDIR -e HBP_INSTANCE_ID -e BASH_ENV=/etc/profile docker-registry.ebrains.eu/hbp-model-validation/docker-ebrains-base

docker push docker-registry.ebrains.eu/hbp-model-validation/docker-ebrains-base