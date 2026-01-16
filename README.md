# MathParser

A lightweight, efficient C library for scanning, parsing, and evaluating simple mathematical expressions using an Abstract Syntax Tree (AST) and returns the output.


## Integration

### Using CMake `FetchContent` (Recommended)
Add this to your `CMakeLists.txt` to automatically download and link the library:

```cmake
include(FetchContent)

FetchContent_Declare(
  MathParser
  GIT_REPOSITORY https://github.com/Thakhinsoelin/MathParser.git
  GIT_TAG        master 
)
FetchContent_MakeAvailable(MathParser)

target_link_libraries(your_app PRIVATE MathParser::MathParser)
```

## Usage
You can simply pass your math expressions which is a C String into double calculate(const char* source);

### example
```C
#include <stdio.h>
#include "Mparser.h"

int main(void) {
    double answer = calculate("-5 * (3 + 4)");
    printf("answer: %s\n", answer); // answer will output -35
    return 0;
}
```
## Grammar Supported

### Unary: - (Negation)

### Binary: +, -, *, / 

### Grouping: ( and ) 


### License
The vector implementation (vec.c) is provided under the BSD 3-Clause License.


---

## Note
Anything that is not supported grammar will be skipped. (eg: characters)