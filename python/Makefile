PROJECT_NAME = max-grape/hello-world/python
WORKDIR      = /usr/src/$(PROJECT_NAME)
REGISTRY     = ghcr.io
IMAGE        = $(REGISTRY)/$(PROJECT_NAME)
TAG          = latest
IMAGE_BUILD  = python:3.9.1-slim

build:
	@docker build \
		--build-arg WORKDIR=$(WORKDIR) \
		--build-arg IMAGE_BUILD=$(IMAGE_BUILD) \
		-t $(IMAGE):$(TAG) .

run:
	@docker run --rm $(IMAGE):$(TAG)
