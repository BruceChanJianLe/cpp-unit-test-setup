REFER TO [cpp-googletest](https://github.com/BruceChanJianLe/cpp-googletest)

# DEPRECATED!
# DEPRECATED!!
# DEPRECATED!!!
# DEPRECATED!!!!

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
But if you would like to use C++ testmate extension you will have to add this line to the `settings.json`
```json
{
    "C_Cpp.default.configurationProvider": "ms-vscode.cmake-tools",
    "C_Cpp.errorSquiggles": "Enabled",
    "testMate.cpp.test.executables": "build-vscode/test/CheckoutTest"
}
```
You will have to provide the absolute path to the file that you would like to test.

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

## WARNINGS

- Always run all tests with ASAN (address sanitizer enabled)
- Always run both Release and Debug builds with ASAN with tests

Ref: https://www.youtube.com/watch?v=4pKtPWcl1Go&ab_channel=C%2B%2BWeeklyWithJasonTurner

## Reference

- Setting up cmake and googletest on vscode [link](https://www.youtube.com/watch?v=Lp1ifh9TuFI)
