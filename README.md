# conan-boost

This sample projects demonstrates using conan to define boost dependency within a c++ project.

This repository can be used as a base project for all c++ development requiring boost and other third party libraries.

```shell
$ conan --version
Conan version 2.7.0
```

## build

```
mkdir build && cd build
conan install .. --build=missing
cmake ..
cmake --build .
cd ..
```
