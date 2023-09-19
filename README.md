To compile C++20 with gcc

```
g++ -std=c++20 -fmodules-ts -x c++-system-header iostream
g++ -std=c++20 -fmodules-ts -o helloworld helloworld.cpp
./helloworld
Hello, World again!

```

and with clang

```
clang++ -std=c++20 -xc++-system-header --precompile iostream -o iostream.pcm
/usr/lib/gcc/aarch64-linux-gnu/12/../../../../include/c++/12/iostream:36:13: warning: #pragma system_header ignored in main file [-Wpragma-system-header-outside-header]
#pragma GCC system_header
            ^
1 warning generated.

clang++ -std=c++20 -fmodule-file=iostream.pcm -o helloworld helloworld.cpp

```


https://www.reddit.com/r/cpp/comments/b3115b/beautiful_c_codebases/

https://stackoverflow.com/questions/4324169/good-open-source-code-for-c

https://news.ycombinator.com/item?id=24901244

https://news.ycombinator.com/item?id=18037613

