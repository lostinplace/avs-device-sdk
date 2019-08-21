add_library(AttachmentCommonTestLib
        Common.cpp)

enable_testing()
find_package(GTest MODULE REQUIRED)

target_include_directories(AttachmentCommonTestLib PUBLIC
        "${AVSCommon_INCLUDE_DIRS}")
target_link_libraries(AttachmentCommonTestLib ${AVSCommon_LIBRARIES})
target_link_libraries(AttachmentCommonTestLib PRIVATE GTest::GTest GTest::Main)
add_test(AllTestsInMain AttachmentCommonTestLib)
