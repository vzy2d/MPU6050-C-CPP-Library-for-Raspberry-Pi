cmake_minimum_required(VERSION 3.0.0)
project(Example VERSION 0.1.0)

include(CTest)
enable_testing()

include_directories(./)
link_directories(./)

add_executable(Example Example.cpp)
target_link_libraries(Example
    MPU6050
    pthread
    )

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
