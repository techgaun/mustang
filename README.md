# mustang
A simple script to convert videos to animated gif

### Installation
You can install mustang by following command:

```shell
$ wget https://raw.githubusercontent.com/techgaun/mustang/master/mustang -O /usr/bin/mustang
$ chmod +x /usr/bin/mustang
```

There's a package called mustang so make sure you don't have it or update installation instruction appropriately.

Alternatively, you can use the docker images to use mustang without having to install ffmpeg or imagemagick on your host OS.
```shell
$ docker run --rm -v /tmp/data:/data techgaun/mustang:alpine -i /data/out.ogv -o /data/out.gif
```

You can alternatively use images based on ubuntu or centos. Just replace `techgaun/mustang:alpine` with `techgaun/mustang:ubuntu` or `techgaun/mustang:centos` however alpine based image is ~85Mb (could be reduced I believe) so ideal.

### Usage
mustang is a simple script that converts videos to animated [gifs](https://en.wikipedia.org/wiki/GIF) using [ffmpeg](https://www.ffmpeg.org/) and [convert](http://www.imagemagick.org) (optionally).

```shell
$ ./mustang -h
mustang - written by techgaun
Usage: mustang [-f <fps_numeric>] -i <input_file> -o <output_file> [-c] [-w]
Example: mustang -f 15 -i /tmp/input.mp4 -o /tmp/output.gif
         mustang -h
Options:
         -c         Enable use of convert command
         -f         Frames per second for gif. Default: 12
         -h         Show help screen
         -i         Input video file
         -o         Output gif file
         -w         Overwrite output file if it exists
```

### To Do

- add high quality switch to create high quality gif
- add transdiff toggle option

### Author
- Samar Acharya <samar@techgaun.com>
