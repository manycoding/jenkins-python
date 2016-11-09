# jenkins-python3
[![](https://images.microbadger.com/badges/image/manycoding/jenkins-python3
.svg)](https://microbadger.com/images/manycoding/jenkins-python3)

## What's Inside

* [jenkins:alpine](https://hub.docker.com/_/jenkins/)
* Python3


## Make It Short 
The [official image repo](https://github.com/jenkinsci/docker) has a pretty comprehensive readme.

To create a master:

    $ docker run -d --name=jenkins -p 8080:8080 -p 50000:50000 -v \
    $home:/var/jenkins_home --env JAVA_OPTS="-Dhudson.footerURL=$server_url \
    -Dhudson.model.DirectoryBrowserSupport.CSP= -Duser.timezone=Europe/Moscow" \
    manycoding/jenkins-python3



To drop into the shell:

    $ docker run --rm -it manycoding/jenkins-python3 /bin/sh
