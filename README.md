# docker-networking

How to implement cross container communication with Docker

## To run this container run the following commands

1. `docker network create favorites-net`
2. `docker run -d --name mongodb --network favorites-net mongo`
3. `docker build -t favorites-node .`
4. `docker run --name favorites -d --rm --network favorites-net -p 3000:3000 favorites-node`
