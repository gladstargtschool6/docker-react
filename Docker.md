

Running Container
```
$ docker run bdcd44a77b05
```

Running Container + Build flagg
```
$ docker run bdcd44a77b05 --build
```

Running Container + Mapping Ports
```
$ docker run -p 3000:3000 bdcd44a77b05
```

Running Container + Mapping Ports + Mapping Folders
```
$ docker run -p 3000:3000 -v $(pwd):/app bdcd44a77b05
```

Running Container + Mapping Ports + Don't Map Folder + Mapping Folder
```
$ docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app bdcd44a77b05
```


Running Tests using the same container + stdin and sudo terminal flagg + overriding command
```
$ docker exec -it bdcd44a77b05 npm run test
```
