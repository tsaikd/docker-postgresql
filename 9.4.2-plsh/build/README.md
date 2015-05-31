How to build binary
===================

* build binary tarball docker image
```sh
docker build -t tsaikd/docker-postgres:9.4.2-plsh-build .
```

* copy binary tarball from docker image

```
docker run -it --rm -v "${PWD}:${PWD}" -w "${PWD}" tsaikd/docker-postgres:9.4.2-plsh-build /install.sh
```

