add_subdirectory("Common")

set(INCLUDE_PATH
	"${AVSCommon_INCLUDE_DIRS}"
  "${AVSCommon_SOURCE_DIR}/AVS/include"
  "${AVSCommon_SOURCE_DIR}/Utils/include"
	"${AVSCommon_SOURCE_DIR}/SDKInterfaces/include"
  "${AVSCommon_SOURCE_DIR}/SDKInterfaces/test"
)

discover_unit_tests("${INCLUDE_PATH}" "AVSCommon;SDKInterfacesCommonTestLib")