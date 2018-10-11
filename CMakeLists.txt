project(mrpt-performance-tests LANGUAGES CXX)
cmake_minimum_required(VERSION 3.3)

# The app:
add_subdirectory(mrpt-perfdata2html)

# --------------------------------
# documentation_performance_html
# --------------------------------
set(PERF2HTML_GENERATED_EXE "$<TARGET_FILE:mrpt-perfdata2html>")
add_custom_target(documentation_performance_html
	COMMAND 		${PERF2HTML_GENERATED_EXE} "${CMAKE_SOURCE_DIR}/perf-data/"
	WORKING_DIRECTORY	${MRPT_SOURCE_DIR}/
	COMMENT 		"Generating performance HTML pages"
	)
add_dependencies(documentation_performance_html mrpt-perfdata2html)
