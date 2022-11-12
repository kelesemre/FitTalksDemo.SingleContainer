# FitTalksDemo.SingleContainer


docker pull mongo
docker run --name another-mongo -d mongo:latest


```docker-compose -f docker-compose.yml -f docker-compose.override.yml up -d```

```docker-compose -f docker-compose.yml -f docker-compose.override.yml up --build```

```docker-compose -f docker-compose.yml -f docker-compose.override.yml down```

## Dockerfile to Image:
```docker build -f FitTalksDemo.SingleContainer.API\Dockerfile --force-rm -t my-fit-api```
## Image to Container
```docker run  --publish 5050:80 --name fit-api-container my-fit-api:latest```

## Hub Actions:
docker login
docker images
Copy tag of the image
docker tag  d2f7cf65ddf0 emrekeless/my-fit-api:dev
docker push emrekeless/my-fit-api:dev

After upload delete all container then
docker pull emrekeless/my-fit-api:dev

Delete the container again
This time create a container on Docker Desktop Interface.
