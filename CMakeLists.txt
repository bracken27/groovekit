cmake_minimum_required(VERSION 3.15)
project(GrooveKit VERSION 1.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# this is the path to your JUCE directory set to your actual path.
if (EXISTS "${CMAKE_SOURCE_DIR}/cmake/JUCEPath.cmake")
    include("${CMAKE_SOURCE_DIR}/cmake/JUCEPath.cmake")
else()
    message(FATAL_ERROR "JUCEPath.cmake not found. Please create it and specify your JUCE directory.")
endif()

# adds JUCE as a subdirectory.
add_subdirectory(${JUCE_DIR} JUCE)

# creates the Executables.
# CLion should create this for you as you add files.
# but make sure this section has your file names.
add_executable(GrooveKit
        src/main.cpp
)

# this is where you link your libraries such as JUCE.
# i've added an example juce library.
target_link_libraries(GrooveKit PRIVATE
        juce::juce_gui_basics
)