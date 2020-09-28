# kdf-node-red
Customized Node Red installation to assist with Home Assistant, when using Inovelli switches.

Based on:
* https://nodered.org/docs/getting-started/docker
* https://github.com/node-red/node-red-docker/blob/master/docker-custom/
* https://flows.nodered.org/node/node-contrib-inovelli-status-manager

## testing locally
```
mkdir ./data
docker build -t kdf-node-red:latest .
docker run -it -p 1880:1880 --name mynodered -v `pwd`/data:/data  kdf-node-red:latest
```

## pushing to dockerhub
```
docker tag kdf-node-red netinept/kdf-node-red
docker push netinept/kdf-node-red
```
