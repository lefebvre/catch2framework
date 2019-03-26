################################################################################
#                                                                              #
#             catch2  TriBITS Package CMakeLists.txt File                      #
#                                                                              #
################################################################################

# This CMakeLists.txt file is being processed as the TriBITS package file.
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR})
TRIBITS_PACKAGE(catch2)
TRIBITS_PACKAGE_DEF()
# Add modules to the cmake module path for ADD_CATCH2_TEST
SET(CMAKE_MODULE_PATH  ${CMAKE_MODULE_PATH} "${catch2_SOURCE_DIR}/cmake")
TRIBITS_PACKAGE_POSTPROCESS()
