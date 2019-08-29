add_subdirectory("Common")

set(INCLUDE_PATH
	"${AVSCommon_INCLUDE_DIRS}"
  "${AVSCommon_SOURCE_DIR}/AVS/include"
  "${AVSCommon_SOURCE_DIR}/Utils/include")

discover_unit_tests("${INCLUDE_PATH}" "AVSCommon;UtilsCommonTestLib")
