PROJECT_NAME = max-grape/hello-world/cpp
WORKDIR      = /usr/src/$(PROJECT_NAME)
REGISTRY     = ghcr.io
IMAGE        = $(REGISTRY)/$(PROJECT_NAME)
TAG          = latest
IMAGE_BUILD  = gcc:9.3.0
IMAGE_FINAL  = scratch

build:
	@docker build \
		--build-arg WORKDIR=$(WORKDIR) \
		--build-arg IMAGE_BUILD=$(IMAGE_BUILD) \
		--build-arg IMAGE_FINAL=$(IMAGE_FINAL) \
		-t $(IMAGE):$(TAG) .

run:
	@docker run --rm $(IMAGE):$(TAG)
