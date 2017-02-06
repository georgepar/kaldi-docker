# kaldi-docker
 Build kaldi inside docker containers with option for CUDA support

To build and run basic kaldi image use the following commands:

```
docker build -t kaldi kaldi/
docker run -ti kaldi
```

To compile Kaldi with CUDA support you must first install the 
[`nvidia-docker` utilities](https://github.com/NVIDIA/nvidia-docker/releases).

Then run

```
nvidia-docker build -t kaldi kaldi-gpu/
nvidia-docker run -ti kaldi
```

You can set the following arguments when building Kaldi:

- `NUM_BUILD_CORES`: The numbers of cores used for the compilation. Default: 8.
- `OPENFST_VERSION`: The version of OpenFST library Kaldi will build against. Default: 1.4.1.

This is based on https://github.com/jbender/docker-kaldi

You can also pull the prebuilt containers from [Docker Hub](https://hub.docker.com/r/georgepar/kaldi/)
