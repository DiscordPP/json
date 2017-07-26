cmake_minimum_required(VERSION 3.6)
project(json)

set(CMAKE_CXX_STANDARD 14)

###################

add_library(${PROJECT_NAME} INTERFACE)
#target_sources(${PROJECT_NAME} INTERFACE "${PROJECT_SOURCE_DIR}/nlohmann/json.hpp")