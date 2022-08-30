PROJECT_NAME = max-grape/hello-world/java
WORKDIR      = /usr/src/$(PROJECT_NAME)
REGISTRY     = ghcr.io
IMAGE        = $(REGISTRY)/$(PROJECT_NAME)
TAG          = latest
IMAGE_BUILD  = openjdk:15.0.2-jdk
IMAGE_FINAL  = openjdk:15.0.2-jdk-slim

build:
	@docker build \
		--build-arg WORKDIR=$(WORKDIR) \
		--build-arg IMAGE_BUILD=$(IMAGE_BUILD) \
		--build-arg IMAGE_FINAL=$(IMAGE_FINAL) \
		-t $(IMAGE):$(TAG) .

run:
	@docker run --rm $(IMAGE):$(TAG)
