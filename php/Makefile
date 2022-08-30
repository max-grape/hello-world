PROJECT_NAME = max-grape/hello-world/php
WORKDIR      = /usr/src/$(PROJECT_NAME)
REGISTRY     = ghcr.io
IMAGE        = $(REGISTRY)/$(PROJECT_NAME)
TAG          = latest
IMAGE_BUILD  = php:7.4-cli

build:
	@docker build \
		--build-arg WORKDIR=$(WORKDIR) \
		--build-arg IMAGE_BUILD=$(IMAGE_BUILD) \
		-t $(IMAGE):$(TAG) .

run:
	@docker run --rm $(IMAGE):$(TAG)
