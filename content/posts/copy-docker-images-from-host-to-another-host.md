---
title: "Copy Docker Images From Host to Another Host"
date: 2017-09-20T17:21:34+05:45
draft: true
---


You will need to save the docker image as a tar file:

```
docker save -o <save image to path> <image name>
```

Then copy your image to a new system with regular file transfer tools such as `cp` or `scp`. After that you will have to load the image into docker:

```
docker load -i <path to image tar file>
```

PS: You may need to `sudo` all commands.
