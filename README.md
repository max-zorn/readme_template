<div align="center">
  
<h1>Service Name</h1>
  
  [![](https://img.shields.io/badge/python-3.9-green.svg?logo=python&logoColor=green)](https://www.python.org/downloads/)
  [![](https://img.shields.io/badge/-cloud%20function-blue?logo=iCloud)]()

**Owner:** Zhukov Max

**Contacts:** [Maxim.Zhukov@softline.com](Maxim.Zhukov@softline.com)

</div>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
## 📖 Description
Simple project description with few examples, schemas and gifs if any.

<br><a href="https://github.com/aregtech/areg-sdk/raw/master/docs/img/areg-services.png"><img src="https://github.com/aregtech/areg-sdk/raw/master/docs/img/areg-services.png" alt="AREG SDK distributed services" style="width:70%;height:70%"/></a><br>



![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
## 🎯 Todo
- [X] One
- [X] Two
- [X] Three
- [ ] Four

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
## 🔗 Links
+ [Confluence](https://adjustcom.atlassian.net/)
+ [ReDoc](http://127.0.0.1:13010/redoc)
+ [Postman](https://)
+ [Production](https://console.cloud.yandex.ru/)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## ☁️ Deployment
To run server:
1. Fill yaml in github actions dir
2. Run workflow 
3. ...
4. Profit

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 💻 Usage

```
java -jar df.jar [OPTIONS] [FLAGS] [COMMANDS]                                 
                                                                              
OPTIONS:                                                                       
   --host <host>            host name, default: localhost                      
   --port <number>          HTTP TCP port number, default: 8080                

                                                                               
FLAGS:                                                                         
   --no-log                 disable request/response console logging           
   --no-log-request-info    disable request info in console logging            
   --no-log-headers         disable request/response headers in console logging
       
                                                                               
COMMANDS:                                                                      
   --help                   print help message                                 
   --print-info             print dump files statistics to stdout as json/yaml 
   --print-requests         print dump requests to stdout as json/yaml         
   --print-openapi          print OpenAPI specification to stdout as json/yaml
```

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🔭 Usage Examples
Start server on dump file:
<pre>
java -jar df.jar --dump dump.txt
</pre>
Start server with built-in OpenAPI client:
<pre>java -jar df.jar --openapi-path /api --dump dump.txt
</pre>

<details>
<summary>
    more examples&hellip;
</summary>
<br>
Start server on few dump files:
<pre>
java -jar df.jar --dump dump1.txt dump2.txt dump3.txt
</pre>
Start server with built-in OpenAPI client with custom title:
<pre>
java -jar df.jar --openapi-path /api --openapi-title 'My REST API v18.2.1' --dump dump.txt
</pre>
</details>
<details>
<summary>
	even more examples&hellip;
</summary>
<br>
Collect live request/response to file:
<pre>
java -jar df.jar --collect /home/john/live.txt --dump dump.txt
</pre>
Specify JSON data file to populate templates:
<pre>
java -jar df.jar --data /home/john/data.json --dump dump.txt
</pre>
Print dump files statistics to stdout as JSON:
<pre>
java -jar df.jar --print-info --dump dump.txt
</pre>
Print dump requests to stdout as JSON:
<pre>
java -jar df.jar --print-requests --dump dump.txt
</pre>
Print OpenAPI specification to stdout as JSON:
<pre>
java -jar df.jar --print-openapi --dump dump.txt
</pre>
</details>
If you still need examples make sure to check out the <a href="Cheatsheet.md">cheatsheet</a>.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🧐 Code analysis
We use some tools to ensure code quality:
+ [flake8](https://github.com/PyCQA/flake8) – code style
+ [isort](https://github.com/timothycrosley/isort) – imports order
+ [mypy](http://mypy-lang.org/) – types annotation
+ [bandit](https://github.com/PyCQA/bandit) – security: our code

To perform all checks, run:
```bash
make check
```

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🧪 Tests
```bash
make test
```

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 📦 Containerization
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

