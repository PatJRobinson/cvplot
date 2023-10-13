cmake_minimum_required(VERSION 3.5)

project(CvPlot)

file(GLOB_RECURSE CVPLOT_SOURCES
  "${CMAKE_CURRENT_SOURCE_DIR}/src/cvplot/*.cpp"
)

file(GLOB_RECURSE CVPLOT_SOURCES_2
  "${CMAKE_CURRENT_SOURCE_DIR}/src/cvplot/*.cc"
)

set(CVPLOT_SOURCES ${CVPLOT_SOURCES} ${CVPLOT_SOURCES_2})

message("SOURCES: ${CVPLOT_SOURCES}")

add_library(${PROJECT_NAME} ${CVPLOT_SOURCES})
target_include_directories(${PROJECT_NAME} PUBLIC include)