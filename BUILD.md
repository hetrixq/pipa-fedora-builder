# Building image

## Run inside a Docker Container

```
docker build -t 'pipa-fedora-builder' . 
docker run --privileged -v "$(pwd)"/images:/build/images -v "/dev:/dev" pipa-fedora-builder
```

### Building Notes

- ```qemu-user-static``` is also needed if building the image on a ```non-aarch64``` system

### Repositories

- [pipa-support](https://copr.fedorainfracloud.org/coprs/spl237/pipa-support/) — kernel and device-specific packages
- [pocketblue](https://copr.fedorainfracloud.org/coprs/onesaladleaf/pocketblue/) — qbootctl for slot switching  