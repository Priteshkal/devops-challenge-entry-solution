VERSION=latest
PREFIX=priteshk1/devops-challenge-entry-particle41
TAG=$(VERSION)

all: build push test

build:
	@echo "Building image:"
	docker build -t $(PREFIX):$(TAG) .
push:
	@echo "Pushing image:"
	docker push $(PREFIX):$(TAG)
test:
	@echo "Running container:"
	docker run --rm -p 80:80 $(PREFIX):$(TAG)