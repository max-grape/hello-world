PROJECT_NAME = max-grape/hello-world/go
WORKDIR      = /usr/src/$(PROJECT_NAME)
REGISTRY     = ghcr.io
IMAGE        = $(REGISTRY)/$(PROJECT_NAME)
TAG          = latest
IMAGE_BUILD  = golang:1.19.0
IMAGE_FINAL  = scratch

build:
	@docker build \
		--build-arg WORKDIR=$(WORKDIR) \
		--build-arg IMAGE_BUILD=$(IMAGE_BUILD) \
		--build-arg IMAGE_FINAL=$(IMAGE_FINAL) \
		-t $(IMAGE):$(TAG) .

run:
	@docker run --rm $(IMAGE):$(TAG)
