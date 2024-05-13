To build a custom image run:

docker build -t custom-name .

to run the custom-image in a container use the following:

docker run -p 3000:80 -d --name container-name --rm custom-image

in the command provided we expose the inner port 80 and 3000 for the app.
-d is used for the container being detached --name gives the
contaner a custom name and --rm removes the container after it stops.
