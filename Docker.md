
# Docker CLI commands

Build Image from a Dockerfile with name:tag
```
$ docker build -t luisgerrarrdo/docker-react
```

Running Container using image tag
```
$ docker run luisgerrarrdo/docker-react
```

Running Container + Build flagg
```
$ docker run luisgerrarrdo/docker-react --build
```

Running Container + Mapping Ports
```
$ docker run -p 3000:3000 luisgerrarrdo/docker-react
```

Running Container + Mapping Ports + Mapping Folders
```
$ docker run -p 3000:3000 -v $(pwd):/app luisgerrarrdo/docker-react
```

Running Container + Mapping Ports + Don't Map Folder + Mapping Folder
```
$ docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app luisgerrarrdo/docker-react
```


Running Tests using the same container + stdin and sudo terminal flagg + overriding command
```
$ docker exec -it luisgerrarrdo/docker-react npm run test
```
