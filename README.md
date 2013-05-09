Audio Fundamentals
=================

## Source code for hands on session for an audio fundamentals workshop ##





### Download PortAudio Nightly Snapshot
`curl -O http://www.portaudio.com/archives/pa_snapshot.tgz`


### Unzip 
`tar -xf pa_snapshot.tgz`

### Compile PortAudio
```
cd portaudio
CFLAGS=-w ./configure --disable-mac-universal --disable-shared && make
```

### Move libportaudio
`cp ./lib/.libs/libportaudio.a ./lib`


### Copy Makefile to examples
`cp ../examples/Makefile ./examples`



