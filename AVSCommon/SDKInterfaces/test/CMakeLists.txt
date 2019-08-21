add_library(SDKInterfacesTests
        src/EqualizerStorageInterfaceTest.cpp
        src/StubMiscStorage.cpp
        )

enable_testing()
find_package(GTest MODULE REQUIRED)

target_include_directories(SDKInterfacesTests PUBLIC ${AVSCommon_INCLUDE_DIRS})

target_link_libraries(SDKInterfacesTests ${AVSCommon_LIBRARIES})
target_link_libraries(SDKInterfacesTests PRIVATE GTest::GTest GTest::Main)
add_test(AllTestsInMain main)

