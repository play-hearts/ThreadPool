## CMake support

You can include ThreadPool in a CMake project as an `INTERFACE` library using
`FetchContent` like this:

```
include(FetchContent)

FetchContent_Declare(
    threadpool
    GIT_REPOSITORY https://github.com/play-hearts/ThreadPool.git
    GIT_TAG da1993d57c7d240ffbcd64fa7a481195a5504157
)

FetchContent_MakeAvailable(threadpool)
```

This defines one library target `ThreadPool`, which can be used like this:

```
add_executable(my_app my_app.cpp)
target_link_libraries(my_app ThreadPool)
```

Include the `ThreadPool` header using

```
#include <ThreadPool.h>
```

(Or as "ThreadPool.h" if you prefer)
