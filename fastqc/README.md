# Docker container for Babraham's fastqc 

Run like so:

```
$ docker run -v ${HOME}:/sourcedata/ -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY -it --rm --name fastqc sthysel/fastqc
```

Note that the host ~/home is available under /sourcedata in the fastqc file open dialog.

http://www.bioinformatics.babraham.ac.uk/projects/fastqc/