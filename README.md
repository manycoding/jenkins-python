# jenkins-python
[![](https://images.microbadger.com/badges/image/manycoding/jenkins-python
.svg)](https://microbadger.com/images/manycoding/jenkins-python)

## Tags

* latest [(Dockerfile)](https://github.com/manycoding/jenkins-python/blob/master/Dockerfile)

## What's Inside

* [jenkins/jenkins:lts-alpine](https://hub.docker.com/r/jenkins/jenkins/)
* Python3

## Make It Short 
The [official image repo](https://github.com/jenkinsci/docker) has a pretty comprehensive readme.

To create a master:

    $ docker run -d --name=jenkins -p 8080:8080 -p 50000:50000 -v \
    jenkins_home:/var/jenkins_home --env JAVA_OPTS="-Dhudson.footerURL=$server_url \
    -Dhudson.model.DirectoryBrowserSupport.CSP= \
    -Duser.timezone=Europe/Moscow" \
    manycoding/jenkins-python

To drop into the shell:

    $ docker run --rm -it manycoding/jenkins-python /bin/sh


## Third-party python libraries

Install with pipenv and export `requirements.txt`

```
pipenv update
pipenv lock -r > requirements.txt
```
