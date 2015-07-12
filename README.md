centos6-devtoolset-3-rpmbuild Dockerfile
=====================================================

The original purpose was a way to build [io.js](https://github.com/nodejs/io.js) for centos 6 repeatably using:
```
docker run --rm -v ${WORKSPACE}:/iojs -w /iojs -t devtoolset-3 ./tools/rpm/rpmbuild.sh
```

Based on:

https://github.com/sclorg/rhscl-dockerfiles/tree/master/centos6.devtoolset-3-toolchain

How to build this Dockerfile
----------------------------

To build the Dockerfile, run:

```
# docker build -t devtoolset-3 .
```

General container help
----------------------

Run `docker run THIS_IMAGE container-usage` to get this help.

Run `docker run -ti THIS_IMAGE bash` to obtain interactive shell.

Run `docker exec -ti CONTAINERID container-entrypoint` to access already running container.

In order to get the container ID after running the image, pass `--cidfile=`
option to the `docker run` command. That will instruct Docker to write
a file with the container ID.

You may try `-e CONT_DEBUG=VAL` with VAL up to 3 to get more verbose debugging
info.
