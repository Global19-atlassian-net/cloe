cmake_minimum_required(VERSION 3.7 FATAL_ERROR)

project(cloe_plugin_noisy_sensors LANGUAGES CXX)

include(${CMAKE_CURRENT_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

include(CloePluginSetup)
cloe_add_plugin(
    TARGET component_noisy_object_sensor
    SOURCES
        src/noisy_object_sensor.cpp
    LINK_LIBRARIES
        CONAN_PKG::cloe-runtime
        CONAN_PKG::cloe-models
)
cloe_add_plugin(
    TARGET component_noisy_lane_sensor
    SOURCES
        src/noisy_lane_sensor.cpp
    LINK_LIBRARIES
        CONAN_PKG::cloe-runtime
        CONAN_PKG::cloe-models
)
