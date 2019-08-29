find_package(GTest MODULE REQUIRED)

add_library(SDKInterfacesCommonTestLib
  StubMiscStorage.cpp
)
target_include_directories(SDKInterfacesCommonTestLib 
  PUBLIC
    "${AVSCommon_INCLUDE_DIRS}"
  	"${AVSCommon_SOURCE_DIR}/Utils/test"
    "${AVSCommon_SOURCE_DIR}/SDKInterfaces/test"
)
target_link_libraries(SDKInterfacesCommonTestLib ${AVSCommon_LIBRARIES})
target_link_libraries(SDKInterfacesCommonTestLib PRIVATE GTest::GTest)