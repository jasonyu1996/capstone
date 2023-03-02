## Capstone

This repository contains the functional prototypes CapstoneEmu (in `emulator`), 
CapstoneC (in `compiler`), and CapstoneLib (in `compiler/samples/capstone.h`),
as well as the GEM5 model used for evaluation (in `gem5`).

Make sure that you update the submodules, either by supplying
`--recurse-submodules` when you clone this repository, or with
```
git submodule update --init --recursive
```
afterwards.

### Build and run the functional prototypes with Docker

The build and run processes for the functional prototypes
have been fully Dockerised. To build all components into a Docker image, make sure you have Docker
installed, and run
```
./build
```

To run with a given source file, use
```
./run <path-to-source-file>
```

You can try with the sample code in `compiler/samples` first.

### GEM5 model

The GEM5 model has likewise been Dockerised.
Please read `gem5/README.md` for detailed instructions.

