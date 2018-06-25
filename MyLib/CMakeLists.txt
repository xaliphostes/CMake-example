cmake_minimum_required(VERSION 3.5)

project(mylib)

############################################################
# Create a library
############################################################

#Generate the shared library from the library sources
add_library(mylib SHARED 
    src/Hello.cxx
    src/common.cxx
)
add_library(hello::library ALIAS mylib)

IF (WIN32)
  add_definitions( -DMYLIB_EXPORTS=TRUE )
  message(--\ Win32\ mode\ activated\ to\ export\ symbols)
ENDIF()

# set the install directory

#install (TARGETS mylib DESTINATION ${PROJECT_SOURCE_DIR}/../bin)

install(TARGETS mylib
     RUNTIME DESTINATION ${PROJECT_SOURCE_DIR}/../bin 
     LIBRARY DESTINATION ${PROJECT_SOURCE_DIR}/../lib 
     ARCHIVE DESTINATION ${PROJECT_SOURCE_DIR}/../lib COMPONENT libraries
)

target_include_directories(mylib
    PUBLIC 
        ${PROJECT_SOURCE_DIR}/include
)
