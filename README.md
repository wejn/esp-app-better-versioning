# ESP-IDF app versioning using build timestamp and git info

For background info see
[this post](https://wejn.org/2025/01/howto-timestamp-and-githash-esp32-firmware-builds/).

The main thing you probably want is the `version.cmake`, and
maybe take a look at `CMakeLists.txt` and `main/CMakeLists.txt`
on how to hook it up.

## Compilation of the example

To compile (in docker):

``` sh
./in-docker.sh idf.py build
```

You should be getting something like:

``` sh
$ idf.py build
Executing action: all (aliases: build)
Running ninja in directory /project/build
Executing "ninja all"...
[0/1] Re-running CMake...
-- Project Version: 20250302082422-ba4f112-dirty
-- Date code: 20250302082422
-- Git rev: ba4f112-dirty
[...]
-- App "hello_world" version: 20250302082422-ba4f112-dirty
[...]
```
