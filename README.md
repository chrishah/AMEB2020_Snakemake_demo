# AMEB2020_Snakemake_demo

## Welcome back!

This page is very much under construction, so please bear with me.

To follow along you are going to need a certain setup on your computer. The easiest way to achieve that is to use an existing Docker image (kindly provided by my esteemed colleage [@reslp](https://github.com/reslp/dockerfiles/blob/master/snakemake/Dockerfile). To use this you're going to need Docker installed on your computer.

Once you have Docker running you can download the image like so:
```bash
(user@host)-$ docker pull reslp/smsi_ubuntu:v1
```

Once you have this you can start the container like so:
```bash
(user@host)-$ docker run -it --rm -v $(pwd):/data --entrypoint /bin/bash reslp/smsi_ubuntu:v1
```

In the first part of the session we're going to follow some material that has been developed for a course on Reproducible research that has been cancelled unfortunately due to Corona. Nevertheless the developers kindly made their material available [here](https://nbis-reproducible-research.readthedocs.io/en/devel/).



For the second part, we're going to need to start the container in a different way, so first, please exit the running container.
```bash
(user@host)-$ exit
```

Then restart, but giving the container extra privileges (I'll explain why we need this in a sec):
```bash
(user@host)-$ docker run --privileged -it --rm -v $(pwd):/data --entrypoint /bin/bash reslp/smsi_ubuntu:v1
```

