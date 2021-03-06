# Yet Another Config Library for C++

### About
YACL is a library for operating configs with large and complex hierarchy. Library is designed to be as simple as possible to read configs and operate on them in code.

### Tested OS/Compilers
 - Windows 10, MSVC 1914
 - Ubuntu 16.04, Clang 5.0.1
 - Ubuntu 16.04, G++ 5.4.0


### Installation
YACL is using cmake to build the project.

Build example provided below
```sh
$ mkdir build
$ cd build
$ cmake .. && cmake --build .
```

### Documentation
All documentation can be found in doc/ folder.
It's generated with doxygen.

### Usage
```cpp 
#include <YACL/config.h>
int main() {
  const yacl::SettingsUniquePtr root = yacl::Config::parseConfigFromFile("config.yacl");
  yacl::Config::printConfig(*root);

  int var1 = *root->field("var1");
  std::string var2 = *root->field("var2");
  std::string var3 = *root->field("var3");

  return 0;
}
```

Other examples can be found in example/ folder.



### Todo List

 - Add gtest
 - Add write functionality
 - Matrix type support
 - Python, Java, ObjC wrappers
 - Add crypt and convert to binary
