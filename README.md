# bazel-golang-hello-world

A minimal example shows how to use bazel with golang.
Try

```
bazel run hello:hello
```

If you want to build a Docker image and test it locally, try

```
bazel build -c opt hello:hello_image.tar
sudo docker load -i bazel-bin/hello/hello_image.tar
sudo docker run bazel/hello:hello_image
```
