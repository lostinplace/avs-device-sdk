cmake_minimum_required(VERSION 3.1 FATAL_ERROR)

find_package(CURL ${CURL_PACKAGE_CONFIG})

add_definitions("-DACSDK_LOG_MODULE=capabilitiesDelegate")
add_library(CapabilitiesDelegate SHARED
    CapabilitiesDelegate.cpp)
target_include_directories(CapabilitiesDelegate PUBLIC
    ${CapabilitiesDelegate_SOURCE_DIR}/include)
target_include_directories(CapabilitiesDelegate PRIVATE)
find_package(rapidjson REQUIRED)
find_package(curl REQUIRED)
target_link_libraries(CapabilitiesDelegate AVSCommon ACL RegistrationManager curl rapidjson)

# install target
asdk_install()
