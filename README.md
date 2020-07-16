# CPP Unit Test Setup

This is a Unit Test setup with cmake which anyone can start their testing work with. It can also act as a reference for future work.

Do note that setting up any unit test you would have to clone the unit test repository `https://github.com/google/googletest.git`.

## Runing and Testing

If you use terminal:
```
mkdir build
cd build
cmake ..
make
```

If you use vscode, just use the cmake tool extension instead.

## Folder structure

```
.
├── CMakeLists.txt
├── googletest
├── include
│   └── Checkout
│       └── Checkout.hpp
├── README.md
├── src
│   └── Checkout.cpp
└── test
    ├── CheckoutTest.cpp
    └── CMakeLists.txt

30 directories, 264 files
```

- include directory is where all the header files are at (main header files to be tested)
- src directory is where all the source files are at (main source file to be tested)
- test directory is where the unit test files are at

## Location of Unit Test Executable

```
cpp-unit-test-setup/build-vscode/test
```

If you do not file it there, mean you have not make it. Do a `make` command will do (if the make files are there).