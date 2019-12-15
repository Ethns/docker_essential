# Docker 18.09 in ubuntu 18.04
## run docker command line with our `sudo`, after add current linux user into docker group, use below command to make it take effect
newgrp docker 
## Common Docker commands:
### start up an Apache server in dettach mode, so you could continue your work
`docker container run -d -it -p 8080:80 httpd`
### check what containers are running
`docker contianer ps / docker ps`
### sync a folder/file in Apache httpd server container with a folder/file on host machine
`docker container run -d -p 8080:80 -v $(pwd)://usr/local/apache2/htdocs -name my-httpd-with-customized-index-html httpd`
### login to a container with bash shell, my-httpd is the name of the target container
`docker container exec -it my-httpd bash`
### more `docker container run` command line operaitoins/arguments
https://docs.docker.com/v18.09/engine/reference/commandline/container_run/#options
`--interactive , -i		Keep STDIN open even if not attached`
`--tty , -t		Allocate a pseudo-TTY`