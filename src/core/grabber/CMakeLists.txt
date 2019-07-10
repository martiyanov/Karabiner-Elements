cmake_minimum_required (VERSION 3.9)

include (../../common.cmake)

project (karabiner_grabber)

include_directories(
  ./include
)

add_executable(
  karabiner_grabber
  MACOSX_BUNDLE
  src/main.cpp
)

set_target_properties(
  karabiner_grabber
  PROPERTIES
  MACOSX_BUNDLE_INFO_PLIST
  ${CMAKE_CURRENT_LIST_DIR}/Resources/Info.plist.in
)

target_link_libraries(
  karabiner_grabber
  "-framework CoreFoundation"
  "-framework CoreGraphics"
  "-framework CoreServices"
  "-framework IOKit"
  "-framework SystemConfiguration"
  c++
)
