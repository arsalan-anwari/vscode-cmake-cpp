cmake_minimum_required( VERSION 3.2 )

## Load CMAKE configuration from environment variables
set( CMAKE_MODULE_PATH $ENV{CMAKE_MODULE_PATH} )
set( CMAKE_PREFIX_PATH $ENV{CMAKE_PREFIX_PATH} )

## Set global variables
set ( PROJECT_NAME_ "app" )

## Specify a project name
project( ${PROJECT_NAME_} )
                       
## Set global definitions to be used in c++
# add_definitions(-DGLEW_STATIC)

## Link Subdirectory 
add_subdirectory(${PROJECT_SOURCE_DIR}/src bin)