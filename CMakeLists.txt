cmake_minimum_required (VERSION 2.6)
project (Tutorial)
# The version number.
set (Tutorial_VERSION_MAJOR 1)
set (Tutorial_VERSION_MINOR 0)

# add the executable
add_executable(Tutorial tutorial.cxx)

# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
  TutorialConfig.h.in
  ../TutorialConfig.h
  )

# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
target_include_directories(Tutorial PUBLIC "${PROJECT_BINARY_DIR}")
 