# Library microservices config server

## Release

```bash
git tag v0.1.x
export IMAGE_TAG=$(git describe --abbrev=0 --tags)

docker build -t rafaelshayashi/library-microservices-config-server:$IMAGE_TAG
docker build -t rafaelshayashi/library-microservices-config-server:$IMAGE_TAG -f cloud/docker/Dockerfile .

docker tag rafaelshayashi/library-microservices-config-server:$IMAGE_TAG rafaelshayashi/library-microservices-config-server:latest

docker push rafaelshayashi/library-microservices-config-server:$IMAGE_TAG
docker push rafaelshayashi/library-microservices-config-server:latest
```