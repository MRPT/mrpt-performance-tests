#-----------------------------------------------------------------
# CMake file for the MRPT application:  mrpt-perfdata2html
#
#  Run with "cmake ." at the root directory
#
#  October 2007, Jose Luis Blanco <jlblanco@ctima.uma.es>
#-----------------------------------------------------------------
project(mrpt-perfdata2html)

# Find MRPT:
find_package(MRPT REQUIRED serialization io system)

# ---------------------------------------------
# TARGET:
# ---------------------------------------------
# Define the executable target:
add_executable(${PROJECT_NAME}
	mrpt-perfdata2html-main.cpp
	)

# Add the required libraries for linking:
target_link_libraries(${PROJECT_NAME} ${MRPT_LIBS})
