
# Science Notebook Dockerfile

Jupyter lab with kernels for Python, R, Julia, Scilab, and maxima.

## Build

You can also pull the image from docker.io.

 $ podman build --rm --force-rm -t --format docker enriquepablo/sciall-nb:1.0.0 .

## Run

Run a container, exposing the notebook at localhost:8888,
and keeping the work in a local directory at /some/local/directory.

 $ podman run -ti --rm --name scilab-nb -p 8888:8888 -v /some/local/directory:/home/sci/nb enriquepablo/sciall-nb:1.0.0
