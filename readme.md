# Conan C++ Package Manager test

## Compiling Required libraries

Conan saves dependencies in `conanfile.txt`. In this case we are going to install Wt library and relative dependencies.

```
mkdir build
cd build 
conan install ..
```

This will populate the build folder with configuration files.

```
cmake .. -U"Unix Makefiles"
```

This will create the build files following `CMakeLists.txt`

```
cmake --build .
```

in `build/bin` you should have your executable `main_exe`

## Running Wt demo

Wt is a c++ library to create web applications in pure C++, using signals and events instead of classic http requests.

To start the demo 
```
./main_exe --docroot . --http-address 0.0.0.0 --http-port 3000
```

You should be able to visualize the demo at [http://localhost:3000](http://localhost:3000)
