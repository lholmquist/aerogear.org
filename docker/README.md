# Previewing AeroGear.org with Jekyll using Docker

Build Docker image (have to be sudo)
```
sudo docker build --tag aerogear.org .
```
If you want to edit files locally you will need to mount your volume at /home/aerogear/aerogear

For example : 
``` 
docker run --rm -it -p 4000:4000 -v /home/user/Projects/aerogear.org:/home/aerogear/aerogear aerogear.org 
```

/home/user/Projects/aerogear.org should be a CLEAN checkout of aerogear.org, otherwise the vendor and bundler dependencies will conflict with those installed in the host system.
