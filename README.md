# About

Little test to slim down .NET core Docker images and build for ARM64.

# Building and running

## Normal x64
- docker build -t test-normal -f Dockerfile-normal .
- docker run -it test-normal

## Alpine x64
- docker build -t test-alpine -f Dockerfile-alpine .
- docker run -it test-alpine  

## Alpine arm64
- docker buildx create --name mybuilder --use
- docker buildx inspect --bootstrap
- docker buildx build --platform=linux/arm64 -t test-alpine-arm -f Dockerfile-alpine-arm . --load
- docker run --platform=linux/arm64 -it test-alpine-arm