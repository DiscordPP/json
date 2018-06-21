cmake_minimum_required(VERSION 3.6)
project(json)

set(CMAKE_CXX_STANDARD 14)

###################

add_library(${PROJECT_NAME} INTERFACE)

#[[
cmake_minimum_required(VERSION 3.0.0)

##
## PROJECT
## name and version
##
project(nlohmann_json VERSION 3.1.2 LANGUAGES CXX)

##
## INCLUDE
##
##
include(ExternalProject)

##
## CONFIGURATION
##
set(NLOHMANN_JSON_TARGET_NAME               ${PROJECT_NAME})
set(NLOHMANN_JSON_TARGETS_EXPORT_NAME       "${PROJECT_NAME}Targets")
set(NLOHMANN_JSON_CMAKE_CONFIG_DIR          "${CMAKE_CURRENT_BINARY_DIR}/cmake_config")
set(NLOHMANN_JSON_CMAKE_VERSION_CONFIG_FILE "${NLOHMANN_JSON_CMAKE_CONFIG_DIR}/${PROJECT_NAME}ConfigVersion.cmake")
set(NLOHMANN_JSON_CMAKE_PROJECT_CONFIG_FILE "${NLOHMANN_JSON_CMAKE_CONFIG_DIR}/${PROJECT_NAME}Config.cmake")


set(NLOHMANN_JSON_INCLUDE_BUILD_DIR "${PROJECT_SOURCE_DIR}/single_include/")
message(STATUS "Using the single-header code from ${NLOHMANN_JSON_INCLUDE_BUILD_DIR}")

##
## TARGET
## create target and add include path
##
add_library(${NLOHMANN_JSON_TARGET_NAME} INTERFACE)

target_include_directories(
    ${NLOHMANN_JSON_TARGET_NAME}
    INTERFACE
    $<BUILD_INTERFACE:${NLOHMANN_JSON_INCLUDE_BUILD_DIR}>
    $<INSTALL_INTERFACE:include>
)
]]