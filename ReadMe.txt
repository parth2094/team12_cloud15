1) Install Docker Engine
Steps:

sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

Open the /etc/apt/sources.list.d/docker.list and add an entry for your Ubuntu operating system. For Ubuntu14.04, it is:

deb https://apt.dockerproject.org/repo ubuntu-precise main

sudo apt-get update

sudo apt-get install docker-engine


2) Install Compose 

curl -L https://github.com/docker/compose/releases/download/1.5.1/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose

3) Then download WordPress into the current directory, using:
	
	curl https://wordpress.org/latest.tar.gz | tar -xvzf -

3) Move the files Dockerfile, docker-compose.yml and wp-config.php to the newly created directory 'wordpress'. 

4) Run the command 
	
	docker-compose up

inside your WordPress directory and it’ll pull and build the needed images, and then start the web and database containers.
