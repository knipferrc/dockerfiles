# Dockerfiles

### devbox
- Pull the image: `docker pull knipferrc/devbox`
- Change into your projects directory
- `docker run --rm -it -v $PWD:/home/devbox/work -p 3000:3000 knipferrc/devbox`
- This image contains: Node, NPM, Go, Meteor, Python2, Python3,
  create-react-app, firebase-tools, gcc, g++, and vim.
