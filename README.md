# Usage

```C++
#include "logger.hpp"
int main(){
  LOGHERE;
  LOGWITH('a',1,2.5f,3);
}
```

### stdout
```
a.cpp:3 main
a.cpp:4 main a 1 2.5 3
```

This uses `std::cout`, so `operator<<(std::ostream&, const T&)` needed.

To print hexadecimal or octal, use it like this
```C++
LOGWITH(std::hex,16,255,std::oct,10,std::dec,100); // out: a.cpp:35 main  10 ff  12  100
```
