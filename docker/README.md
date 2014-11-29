# Git

This is a cross between a tutorial, a checklist and a cheatsheet:

  * a summary, hopefully a memorable declarative sentence

  * a quick tutorial, ideally with some visuals and with some "layout"

  * a query

  * an action or setting

  * a "follow up", either the query again, or a test or an example (or any combination of these).

  * some observations, opinions or "lore" mixed together

  * references

    - {internally, externally} {prior, subsequent}

    - additional kinds of relationships (to be supplied)

  * opinionated


## Installation

Install directly from docker.io, one of several [ubuntu approaches](https://docs.docker.com/installation/ubuntulinux/) the easiest way:

```bash
curl -sSL https://get.docker.com/ | sh # install, trust the internet
service docker status # service says docker's running (?)
ps aux|ag 'docker -d' # ... or you can look for the process itself
docker info
```

`lxc-docker` actually got installed:

```bash
dpkg-query --list lxc-docker # should find docker
dpkg-query -L lxc-docker-1.3.1 # or your version
```


## Configuration

Docker root:

```bash
export DOCKER_ROOT=$(dirname $(docker info|grep ' Root Dir:'|cut -c12-))
echo ${DOCKER_ROOT} # /var/lib/docker
```

