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

## 💻 Deployment
To run server:
1. Start 
2. Run postgres (locally or in docker) and create a DB there, see details on [Confluence](https://adjustcom.atlassian.net/)
3. Copy `.env.sample` to `.env`. Make sure DATABASE_URL is a valid link to the DB dedicated to this service.
4. Run `make start`

## 🚀 Usage

```
java -jar df.jar [OPTIONS] [FLAGS] [COMMANDS]                                 
                                                                              
OPTIONS:                                                                       
   --host <host>            host name, default: localhost                      
   --port <number>          HTTP TCP port number, default: 8080                
   --port-ssl <number>      HTTPS TCP port number, default: 8443               
   --dump <file|url>...     dump text file(s)/URL(s)
   --db <file|url>          json/yaml/csv memory file to populate templates    
   --db-export <file>       export memory to json file                         
   --db-path <path>         serve live memory file at specified context        
   --dir <dir>              forward unmatched requests to specified directory            
   --js <file|url>...       JavaScript file(s) for script engine context       
   --openapi-path <path>    serve built-in OpenAPI client at specified context 
   --openapi-title <text>   provide custom OpenAPI specification title         
   --collect <file>         collect live request/response to file              
   --format <json|yaml>     output format for --print-* commands, default: json
   --status <number>        status code for non-matching requests, default: 404
   --max-log-body <number>  max body bytes in console log, default: unlimited  
                                                                               
FLAGS:                                                                         
   --no-log                 disable request/response console logging           
   --no-log-request-info    disable request info in console logging            
   --no-log-headers         disable request/response headers in console logging
   --no-log-body            disable request/response body in console logging   
   --no-cors                disable CORS headers                               
   --no-etag                disable 'ETag' header                              
   --no-server              disable 'Server' header                            
   --no-watch               disable watch files for changes                    
   --no-color               disable ANSI color output for --print-* commands   
   --no-pretty              disable prettyprint for --print-* commands         
   --no-template            disable template processing                        
   --no-wildcard            disable wildcard processing                        
   --no-bak                 disable backup old memory file before overwrite    
   --strict-json            enable strict JSON comparison                      
   --redirect               enable redirect HTTP to HTTPS                      
   --db-export-on-exit      export memory only on server close event           
                                                                               
COMMANDS:                                                                      
   --help                   print help message                                 
   --print-info             print dump files statistics to stdout as json/yaml 
   --print-requests         print dump requests to stdout as json/yaml         
   --print-openapi          print OpenAPI specification to stdout as json/yaml
```

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

