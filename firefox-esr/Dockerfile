FROM alpine:latest
LABEL original.github "https://github.com/mrorgues/dockerfiles"

# docker run --rm -it \
#   --net host \
#   -v /tmp/.X11-unix:/tmp/.X11-unix \
#   -e DISPLAY=unix$DISPLAY \
#   --device /dev/dri \
#   --device /dev/snd \
#   -v /dev/shm:/dev/shm \
#   -v /etc/fonts:/etc/fonts \
#   -v /etc/machine-id:/etc/machine-id \
#   -v /usr/share/fonts:/usr/share/fonts \
#   -v $HOME/.mozilla:/root/.mozilla \
#   --ipc="host" \
#   --name firefox-esr \
#   mrorgues/firefox-esr

RUN  apk add --no-cache \
        ca-certificates \
        firefox-esr \
        libcanberra-gtk2 && \
        rm -rf /tmp/* 

ENTRYPOINT [ "/usr/bin/firefox" ]