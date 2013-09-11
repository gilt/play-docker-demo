#Play Docker Demo

This is a very simple demo to show how you can run a Docker container that runs
a [simple](https://github.com/rolandtritsch/scala-play-hello)
Scala Play App.

* Install docker -- http://www.docker.io/
* Clone this repository
* Build the three containers:  
`sudo docker build -t=base base/`  
`sudo docker build -t=play-hello play-hello/`  
`sudo docker build -t=play-hello-run play-hello-run/`
* Run the container   
`sudo docker -h=localhost run play-hello-run`
* Load the URL below into your browser:  
http://$hostname/$ip:9001/name/Docker