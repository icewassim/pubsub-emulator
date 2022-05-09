# Google PubSub Emulator Docker Image

# Usage

```
$ docker pull icewassim/pubsub-emulator:latest
$ docker run --rm -ti --name pubsub-emu pubsub
```

Or in a `docker-compose.yml`

```
pubsub:
  image: icewassim/pubsub-emulator
worker:
  build: .
  environment:
    - PUBSUB_EMULATOR_HOST=pubsub:8085
  restart: always
  links:
    - pubsub
```
