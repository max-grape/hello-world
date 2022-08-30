PROJECT_NAME = max-grape/hello-world/csharp
WORKDIR      = /usr/src/$(PROJECT_NAME)
REGISTRY     = ghcr.io
IMAGE        = $(REGISTRY)/$(PROJECT_NAME)
TAG          = latest
IMAGE_BUILD  = mono:6.12.0.107
IMAGE_FINAL  = mono:6.12.0.107-slim

build:
	@docker build \
		--build-arg WORKDIR=$(WORKDIR) \
		--build-arg IMAGE_BUILD=$(IMAGE_BUILD) \
		--build-arg IMAGE_FINAL=$(IMAGE_FINAL) \
		-t $(IMAGE):$(TAG) .

run:
	@docker run --rm $(IMAGE):$(TAG)
