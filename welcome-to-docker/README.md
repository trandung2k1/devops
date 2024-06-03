### Build image -t: image_name, -f: name_docker_file

```sh
docker build -t trandung2001/welcome-to-docker:v1 .
```

### Run image mode: -it, -d; -rm: auto remove container; --name: name_container; -p: port_app_local:port_container

```js
docker run -it --rm --name welcome-to-docker -p 8080:3000 trandung2001/welcome-to-docker:v1
```

### Run image exit cmd

```js
docker run -d --name welcome-to-docker -p 8080:3000 trandung2001/welcome-to-docker:v1
```

### Login docker: username and password docker hub

```bash
docker login
```

### Push docker image

```js
docker push trandung2001/welcome-to-docker:v1
```

### Exec container

```js
docker exec -it welcome-to-docker sh
```
