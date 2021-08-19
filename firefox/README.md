#Firefox in a Docker Container

So, a few years ago, I had a buddy that I won't dox that was an absolute beast
that used to run cgroup chroots, doing a docker before docker was docker.

So what he did was he used multiple instances of firefox, with their own VPNs,
and scripted it. Like a docker. He was able to run multiple instances of Firefox
from around the world, right from one same X session on a desktop. And it
worked!

This was some elite badassery.

This is both a tribute and a simple container to practice writing Dockerfiles.
It can work with any distro, but I chose arch because I like it, and because of
rolling release will always be the latest version of firefox.

to compile
```
docker build . -t "firefox-arch"
```

to run
```
docker run -it -e DISPLAY --net=host firefox_archlinux
```
or
```
./run_docker.sh
```
