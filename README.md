<div align="center">
  
<h1>Service Name</h1>
  
  [![](https://img.shields.io/badge/python-3.9-green.svg?logo=python&logoColor=green)](https://www.python.org/downloads/)
  [![](https://img.shields.io/badge/-cloud%20function-blue?logo=iCloud)]()

**Owner:** Zhukov Max

**Contacts:** [Maxim.Zhukov@softline.com](Maxim.Zhukov@softline.com)


</div>

## 📖 Description
Simple project description with few examples, schemas and gifs if any.

## 🎯 Todo
- [X] One
- [X] Two
- [X] Three
- [ ] Four

## 🔗 Links
+ [Confluence](https://adjustcom.atlassian.net/)
+ [ReDoc](http://127.0.0.1:13010/redoc)
+ [Postman](https://)
+ [Production](https://console.cloud.yandex.ru/)

## Development
To run server:
1. Start 
2. Run postgres (locally or in docker) and create a DB there, see details on [Confluence](https://adjustcom.atlassian.net/)
3. Copy `.env.sample` to `.env`. Make sure DATABASE_URL is a valid link to the DB dedicated to this service.
4. Run `make start`

## Code analysis
We use some tools to ensure code quality:
+ [flake8](https://github.com/PyCQA/flake8) – code style
+ [isort](https://github.com/timothycrosley/isort) – imports order
+ [mypy](http://mypy-lang.org/) – types annotation
+ [bandit](https://github.com/PyCQA/bandit) – security: our code

To perform all checks, run:
```bash
make check
```

## Tests
```bash
make test
```

## Containerization
### Docker

You can use docker and docker-compose to work with your project.

To build a docker image, use:
```
docker build --ssh default . -t my-service
```
And run with:
```
docker run my-service
```
Options for docker run are:
- `-d`: Run in detached mode, does not hang your terminal session.
- `--rm`: Removes container after finish
- `-it`: Runs interactively
- `docker run -it --rm my-service <command>`: run a command using the container image

### Additional docker commands
- `docker ps`: Checks docker images running.
- `docker exec -it <container_id> <command>`: Runs a command inside the running container.

