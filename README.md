# Dockerfiles

### devbox
- Pull the image: `docker pull knipferrc/devbox`
- Change into your projects directory
- `docker run --rm -it -v $PWD:/home -p 3000:3000 knipferrc/devbox`
