cmake_minimum_required(VERSION 3.12)
project(untitled)

set(CMAKE_CXX_STANDARD 14)

set(CURL_LIBRARY "-lcurl")
set(LXML_LIBRARY "-lxml2")
find_package(CURL REQUIRED)
find_package(libxml2 REQUIRED)


#add_executable(untitled multilinker.cpp)
#add_executable(untitled test.cpp)
add_executable(untitled main.cpp)
#add_executable(untitled test2.cpp)

include_directories(${CURL_INCLUDE_DIR})
target_link_libraries(untitled ${CURL_LIBRARIES})
target_link_libraries(untitled ${LXML_LIBRARY})




