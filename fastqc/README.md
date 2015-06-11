# Docker container for Babraham's fastqc 

Download the [fastqc](fastqc) script here or just run like so:
```
$ xhost +; docker run -v ${HOME}:/sourcedata/ -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY -it --rm --name fastqc sthysel/fastqc
```

Note that the host ~/home is available under /sourcedata in the fastqc file open dialog.

http://www.bioinformatics.babraham.ac.uk/projects/fastqc/
