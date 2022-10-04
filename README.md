cerebro-docker-arm
--------------

### Note
This project is a fork from [cerebro-docker](https://github.com/lmenezes/cerebro-docker) which supports ARM machine like M1 MacBook Pro.

cerebro-docker contains the official docker files for [cerebro](https://github.com/lmenezes/cerebro) project.
Images are periodically uploaded in [lmenezes/cerebro](https://hub.docker.com/r/lmenezes/cerebro/) docker hub repo.

### Usage

For using latest cerebro execute:

```
docker run -p 9000:9000 crossrt/cerebro-docker-arm
```

For using a specific version run:

```
docker run -p 9000:9000 crossrt/cerebro-docker-arm:0.9.4
```

### Configuration

You can configure a custom port for cerebro by using the `CEREBRO_PORT` environment variable. This defaults to `9000`.

**Example**

docker run -e CEREBRO_PORT=8080 -p 8080:8080 lmenezes/cerebro

To access an elasticsearch instance running on localhost:

docker run -p 9000:9000 --network=host lmenezes/cerebro
