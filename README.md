# JLC 1.0 coming soon !

**Java-Like C++ (JLC) is a light-weight header-only utility library providing easy-to-use types and functions for C++.**

JLC was firstly designed to achieve C++ tasks that were very difficult to do with standard libraries as a first year engineer student.
Some aspects of C++ that are particularly restrictive and difficult for a beginner are date/time, lists, pointers and strings.

In an effort to prevent developper's brain collapsing and nightmares, JLC provides a simple and complete set of classes and methods inspired from Java and JavaScript languages, such as for example the native JavaScript Date and String objects or the Java 8 Collection and Stream containers.
Furthermore, every JLC classes are designed to use as less pointers as possible in production code, which greatly improves developper experience.

This is a small overview of features provided by JLC :

```c++
#include <JLC/JLC.h>
using namespace JLC;

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

In hope that you will love JLC, you will find more information and code examples in the [wiki].
Good reading !

JLC is still under construction ! Keep in touch !

- [ ] array.h
- [ ] calendar.h
- [ ] collection.h
- [ ] containers.h
- [x] debug.h
- [ ] functions.h
- [x] JLC.h
- [ ] list.h
- [ ] map.h
- [ ] queue.h
- [ ] range.h
- [ ] set.h
- [ ] stack.h
- [ ] stream.h
- [ ] string.h

--------------------------------------------------------------------------------

Language support : C++98, C++11, C++14, C++17, C++20.

Compiler support : Clang 1+, GCC 4+.

- [CHANGELOG]
- [LICENSE]
- [WIKI]

*Designed by Baptiste Thémine*

[CHANGELOG]: CHANGELOG.md
[LICENSE]: LICENSE
[WIKI]: https://github.com/Baptistou/JLC/wiki
