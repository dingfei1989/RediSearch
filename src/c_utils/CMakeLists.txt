ADD_EXECUTABLE(sizes sizes.cpp)
ADD_EXECUTABLE(apibench apibench.cpp)
ADD_LIBRARY(apistubs STATIC api_stubs.c)
TARGET_LINK_LIBRARIES(sizes redisearch api_stubs dl)
TARGET_LINK_LIBRARIES(apibench redisearchS redismock api_stubs dl)