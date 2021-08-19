#Firefox in a Docker Container

I just wanted to see if I could run X/Wayland apps in docker. Turns out:

IT WORKS!

to compile
```
docker build . -t "firefox_archlinux"
```

to run
```
docker run -it -e DISPLAY --net=host firefox_archlinux
```
or
```
./run_docker.sh
```
