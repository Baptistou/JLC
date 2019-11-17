# JLC 1.0 coming soon !

**Java-Like C++ (JLC) is a light-weight header-only utility library providing easy-to-use types and functions for C++.**

This is a small overview of features provided by JLC :
```cpp
#include "JLC.h"
using namespace jlc;

int main(){
    String str = "hello dear github user !";
    std::cout << str
        .split(' ')
        .stream()
        .filter([](const String &val){ return (val.length()!=4); })
        .map<String>(&String::toucfirst)
        .collect<collectors::tolist>()
        .join(' ')
        << std::endl;
}
```
```
Hello Github !
```

--------------------------------------------------------------------------------

Compiler support : Clang 1.0+, GCC 4.2.1+.

- [CHANGELOG](CHANGELOG.md)
- [LICENSE](LICENSE)
- [WIKI](https://github.com/Baptistou/JLC/wiki)

*Designed by Baptiste Thémine*
