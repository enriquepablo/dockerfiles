
# Scilab NB 6.1.1 Dockerfile

Jupyter lab with scilab kernel.

## Build

You can also pull the image from docker.io.

 $ podman build --rm --force-rm --format docker -t enriquepablo/scilab-nb:6.1.1 .

## Run

Run a container, exposing the notebook at localhost:8888,
and keeping the work in a local directory at /some/local/directory.

 $ podman run -ti --rm --name scilab-nb -p 8888:8888 -v /some/local/directory:/home/sci/nb enriquepablo/scilab-nb:6.1.1
