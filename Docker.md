# Docker

- General
````
docker build . <in the directory where Dockerfile sits>
docker images <to get image id>
docker run -p 8080:8080 -e CONFIG_SOURCE=local <docker id>
````

- Local redis
````
docker run -it -p 6379:6379 redis
````