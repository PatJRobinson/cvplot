cmake_minimum_required(VERSION 3.5)

project(CvPlot)

file(GLOB_RECURSE CVPLOT_SOURCES
  "${CMAKE_CURRENT_SOURCE_DIR}/src/cvplot/*.cpp"
)

file(GLOB_RECURSE CVPLOT_SOURCES
  "${CMAKE_CURRENT_SOURCE_DIR}/src/cvplot/*.cc"
)

add_library(${PROJECT_NAME} ${CVPLOT_SOURCES})
target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)