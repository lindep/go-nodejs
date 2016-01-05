Docker: Node and Go dev environment
==================================

Build and development environment for Node and Go language

1. Clone repo
```bash
git clone https://github.com/lindep/docker_build_env.git build_dev
```

2. Download Go binaries and extract into go DIR
3. Create docker image
Node will be installed via nvm
```bash
docker build --tag "image_name" .
```

Create Golang dev environment

```bash
mkdir -p ~/go_src/src
mkdir -p ~/go_src/pkg
mkdir -p ~/go_src/bin
```

The GOPATH env variable need to be mapped form /go_path in container 
to a DIR on the host where Go src files are
then start the image

docker run -it -v ~/go_src:/go_path --name dev_image image_name bash
```bash
. ~/.nvm/nvm.sh
nvm use 4
```