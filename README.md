## PyOpenPose

Python bindings for the awesome Openpose library. 

Openpose [github page](https://github.com/CMU-Perceptual-Computing-Lab/openpose)


### Building

Clone and build openpose. I assume you will also build caffe inside openpose 3rdparty folder.
Set an environment variable named OPENPOSE_ROOT pointing to the openpose root folder.

__Note:__ Openpose lib is under heavy development and the API changes very often. 
Some API changes will break PyOpenPose. I try to upgrade as soon as possible but I am usually a few days behind. 
Openning an issue helps to speed-up the proccess. Current PyOpenPose version is built with [openpose commit 1b0325e](https://github.com/CMU-Perceptual-Computing-Lab/openpose/commit/1b0325e2980a43ba2c9612068f78eb1c38d41ee5)

__Note:__ PyOpenPose requires __opencv3.x__. You will have to build openpose with opencv3 as well.

Inside the root folder of PyOpenpose run cmake and build with:

```bash
mkdir build
cd build
cmake ..
make
```

Add the folder containing PyOpenPose.so to your PYTHONPATH.

### Building the library for python3

 - make sure cmake discovers python3 libraries and include dirs. 
 - set cmake to discover the boost_python libs for python3 or set `libboost_python.so` to point to `/usr/lib/x86_64-linux-gnu/libboost_python-py35.so`
 - run the example scripts with python3

### Testing

Check the scripts folder for python examples using PyOpenPose.
