# For more information see the CMake documentation:
# http://www.cmake.org/cmake/help/documentation.html
# http://techbase.kde.org/Development/Tutorials/CMake

# Project name
project(HelloWorld)

# Look for the KArchive module
find_package(KF5Archive ${KF_VERSION} REQUIRED)

find_package(Qt5Core REQUIRED)

add_executable(helloworld main.cpp)

# Link our executable with the KArchive library
target_link_libraries(helloworld KF5::Archive Qt5::Core)
