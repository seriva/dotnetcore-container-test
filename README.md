# About

Little test to slim down .NET core Docker images.

# Building and running

docker build -t test-normal -f Dockerfile-normal .
docker run -it test-normal

docker build -t test-alpine -f Dockerfile-alpine .
docker run -it test-alpine  

docker buildx build --platform=linux/arm64 -t test-alpine-arm -f Dockerfile-alpine-arm .
docker run -it test-alpine-arm  