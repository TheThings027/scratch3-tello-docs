---
title: Build Environment
weight: 10
---

# Build Environment
Scratch3-Tello does not work only with the extension mechanism provided in Scratch. In fact, I've made changes to `scratch-vm`, `scratch-gui`, and `scratch-desktop` that make up Scratch.  
The `scratch3-tello` repository contains the diffs of those changes made, file by file. Therefore, you cannot build just by cloning this repository.

## Requirements
- wget
- git
- node.js
- npm

## Create a working folder
```bash
$ mkdir scratch3-tello
$ cd scratch3-tello
```

## Download the script to build the environment
```bash
$ wget https://raw.githubusercontent.com/kebhr/scratch3-tello/master/build.sh
$ chmod +x build.sh
```

## Run the script to build the environment
```bash
$ ./build.sh
```

Running `build.sh` will automatically clone `scratch-vm`, `scratch-gui`, and `scratch-desktop` and apply the diffs files managed by `scratch3-tello` repository.

## Start Scratch3-Tello
```bash
$ cd scratch-desktop
$ npm run build-gui
$ npm start
```

## Make package
```bash
$ cd scratch-desktop
$ npm run dist:dir
```
