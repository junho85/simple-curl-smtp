cmake_minimum_required(VERSION 3.10)
project(simple_curl_smtp C)

set(CMAKE_C_STANDARD 99)

find_package(CURL REQUIRED)
include_directories(${CURL_INCLUDE_DIRS})
message("-- Found CURL: ${CURL_INCLUDE_DIRS} ${CURL_LIBRARIES}")

add_executable(simple_curl_smtp main.c)

target_link_libraries(simple_curl_smtp
        ${CURL_LIBRARIES}
        )