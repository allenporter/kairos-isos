# kairos-ios

Kairos 
[Kairos](https://github.com/kairos-io/kairos) ISOs built from container images
in https://github.com/allenporter/kairos-distros.


## Building an iso

```bash
$ IMAGE_NAME=ghcr.io/allenporter/kairos-ubuntu-intel-nuc:v0.1.0
$ docker run -v "${PWD}/build:/tmp/auroraboot" \
    --rm -ti quay.io/kairos/auroraboot:v0.2.7 \
    --set "container_image=docker://${IMAGE_NAME}" \
    --set "disable_http_server=true" \
    --set "disable_netboot=true" \
    --set "state_dir=/tmp/auroraboot" \
    --debug
```
