add_library(AttachmentCommonTestLib
        Common.cpp)

target_include_directories(AttachmentCommonTestLib PUBLIC
        "${AVSCommon_INCLUDE_DIRS}"
        "${AVSCommon_SOURCE_DIR}/AVS/include"
        "${AVSCommon_SOURCE_DIR}/Utils/include")
target_link_libraries(AttachmentCommonTestLib ${AVSCommon_LIBRARIES})

