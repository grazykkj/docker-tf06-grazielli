Saída dos comandos solicitados:
```Bash
Creating network "tf-is-aula-06_appnet" with driver "bridge"
Building web
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon   5.12kB
Step 1/3 : FROM nginx:alpine
 ---> d5030d429039
Step 2/3 : COPY nginx/html/index.html /usr/share/nginx/html/index.html
 ---> 13db5a61df2a
Step 3/3 : EXPOSE 80
 ---> Running in 9cd9b87ae41f
 ---> Removed intermediate container 9cd9b87ae41f
 ---> 344e8800a606
Successfully built 344e8800a606
Successfully tagged tf-is-aula-web:latest
WARNING: Image for service web was built because it did not already exist. To rebuild this image you must use `docker-compose build` or `docker-compose up --build`.
Creating tf-is-aula-06_cache_1 ... done
Creating tf-is-aula-06_web_1   ... done
        Name                      Command             State    Ports  
----------------------------------------------------------------------
tf-is-aula-06_cache_1   docker-entrypoint.sh redis    Up      6379/tcp
                        ...                                           
tf-is-aula-06_web_1     /docker-entrypoint.sh sh -    Up      80/tcp  
                        ...                                           
PING cache (172.18.0.2): 56 data bytes
64 bytes from 172.18.0.2: seq=0 ttl=64 time=0.073 ms
64 bytes from 172.18.0.2: seq=1 ttl=64 time=0.083 ms
64 bytes from 172.18.0.2: seq=2 ttl=64 time=0.058 ms

--- cache ping statistics ---
3 packets transmitted, 3 packets received, 0% packet loss
round-trip min/avg/max = 0.058/0.071/0.083 ms
