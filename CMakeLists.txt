################################################################################
#                                                                              #
#             catch2  TriBITS Package CMakeLists.txt File                      #
#                                                                              #
################################################################################

# This CMakeLists.txt file is being processed as the TriBITS package file.
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR})
# required for configured file
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_BINARY_DIR})
TRIBITS_PACKAGE(catch2)
# Add modules to the cmake module path for ADD_CATCH2_TEST
SET(CMAKE_MODULE_PATH  ${CMAKE_MODULE_PATH} "${catch2_SOURCE_DIR}/modules/" PARENT_SCOPE)

TRIBITS_ADD_LIBRARY(catch2main
   SOURCES catch2/catchmain.cc
   NOINSTALLHEADERS catch2/catch.hpp
)
TRIBITS_PACKAGE_POSTPROCESS()
