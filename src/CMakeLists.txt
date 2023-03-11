cmake_minimum_required( VERSION 3.2 )

## Sources and headers
include_directories( ${CMAKE_CURRENT_SOURCE_DIR} )


## Find all source and header files to be compiled into object files
file( GLOB_RECURSE SOURCES *.cc *.hh *.cpp *.hpp *.c *.h )

## Add Libraries


## Find Required Packages


## C++ compiler options

### Compiler settings
set( CMAKE_CXX_FLAGS_DEBUG "-g -O0" )
set( CMAKE_CXX_FLAGS_RELEASE "-O3" )

# Allow warnings 
#set( CMAKE_CXX_FLAGS "-Wall -Wextra -Wno-format -Wno-unused-parameter -Wno-unused-function -mavx2 -std=gnu++20" )

# Make warnings same as errors
set( CMAKE_CXX_FLAGS "-Wall -Wextra -Werror -mavx2 -std=c++17" ) 


## Source file containing the "main" function
set( MAIN_SOURCE main.cpp )
## Specify a name for the generated executable file
set( MAIN_EXE_NAME ${PROJECT_NAME_} )


## 1. Compile...
add_executable( ${MAIN_EXE_NAME} ${MAIN_SOURCE} ${SOURCES} ${ENGINE_SOURCES} )


## 2. Link...
target_link_libraries( ${MAIN_EXE_NAME} )


## 3. Install...
install( TARGETS ${MAIN_EXE_NAME} )
