add_library(AFML SHARED
    AudioActivityTracker.cpp
    Channel.cpp
    FocusManager.cpp
    VisualActivityTracker.cpp)

add_definitions("-DACSDK_LOG_MODULE=afml")
include_directories(AFML "${AFML_SOURCE_DIR}/include")
find_package(RapidJSON CONFIG REQUIRED)
target_link_libraries(AFML AVSCommon)
message(${RAPIDJSON_INCLUDE_DIRS})
target_include_directories(AFML PRIVATE ${RAPIDJSON_INCLUDE_DIRS})

# install target
asdk_install()
