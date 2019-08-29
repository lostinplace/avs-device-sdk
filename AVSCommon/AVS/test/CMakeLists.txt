add_subdirectory("Attachment")
message("**********")
find_package(AVSCommon)
set(INCLUDE_PATH
    "C:/GLORPERDY"
    "${AVSCommon_SOURCE_DIR}/AVS/include"
    "${AVSCommon_SOURCE_DIR}/Utils/include"
    "${AVSCommon_INCLUDE_DIRS}/derp"
    "${AVSCommon_SOURCE_DIR}/AVS/test"
    "${AVSCommon_SOURCE_DIR}/SDKInterfaces/test")

discover_unit_tests("${INCLUDE_PATH}" "AVSCommon;AttachmentCommonTestLib")
