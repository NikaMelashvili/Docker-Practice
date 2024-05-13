# Image / Container custmoazation

To build a custom image run:

`docker build -t custom-name .`

to run the custom-image in a container use the following:

`docker run -p 3000:80 -d --name container-name --rm custom-image`

In the command provided, we expose the inner ports 80 and 3000 for the app. -d is used for detaching the container, --name gives the container a custom name, and --rm removes the container after it stops.

---

# Volumes and Bind mounts

## Volumes

With volumes, we can keep track of the data that's going through Docker. There are anonymous and named volume types. Anonymous volumes are meant for data that's not persistent, while named volumes survive after the container has finished execution.

`docker run -p 3000:80 -d --rm --name feedback-con -v feedback:/app/feedback newer-docker-feedback`

with the command provided we can create a named volume that wont dissapear after the container is deleted and when we launch a new container our data will still be there.

## Bind mounts

bind mounts work the same as volumes but for the project itself:

```bash
 docker run -p 3000:80 -d --rm --name feedback-con -v feedback:/app/feedback -v "D:\Drive\docker practice\data-volumes-01-starting-setup" newer-docker-feedback
```
