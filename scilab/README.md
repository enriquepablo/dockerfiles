
# Scilab 6.1.1 Dockerfile

## Build

You can also pull the image from docker.io.

 $ podman build --rm --force-rm --format docker -t enriquepablo/scilab:6.1.1 .

## Run

Run this on linux (or some other OS with an X server).

Provide access to the X server:

 $ xhost +local:

Run a container, providing it with the local X server.

 $ podman run --rm -d \
   -v /tmp/.X11-unix:/tmp/.X11-unix \
   -e DISPLAY=unix$DISPLAY \
   --name scilab \
   enriquepablo/scilab:6.1.1
