# Play Docker Demo

This is a very simple demo to show how you can run a Docker container that runs a [simple](https://github.com/rolandtritsch/scala-play-hello) Scala Play App.

Just ...

* Install docker and make sure the Docker Hello World example works
* Build the three containers ...
    > cd base; sudo docker build -t=base .; cd ..
    > cd hello-play; sudo docker build -t=play-hello .; cd ..
    > cd play-hello-run; sudo docker build -t=play-hello-run .; cd ..
* Run the container `> sudo docker -h=localhost run play-hello-run`
* Load `http://localhost:9001/name/Docker` into your browser
