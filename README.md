## Capstone

This repository contains the CapstoneEmu (in `emulator`), CapstoneC (in `compiler`),
and CapstoneLib (in `compiler/samples/capstone.h`).
Make sure that you update the submodules, either by supplying
`--recurse-submodules` when you clone this repository, or with
```
git submodule update --init --recursive
```
afterwards.

### Build and run with Docker

The build and run processes have been fully Dockerised. To build all components into a Docker image, make sure you have Docker
installed, and run
```
./build
```

To run with a given source file, use
```
./run <path-to-source-file>
```

You can try with the sample code in `compiler/samples` first.

