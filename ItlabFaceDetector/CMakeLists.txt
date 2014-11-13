CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

set(PROJECT_NAME FaceDetector)
project(${PROJECT_NAME})

find_package(OpenCV REQUIRED)

set(FACEDETECTOR_LIBRARY ${PROJECT_NAME})
set(SOURCE_EXE main.cpp)

set(FACEDETECTOR_INCLUDE "${CMAKE_CURRENT_SOURCE_DIR}/include")
include_directories(${FACEDETECTOR_INCLUDE})

set(LIBRARY_DEPS ${OpenCV_LIBS})

add_executable(main ${SOURCE_EXE})

add_subdirectory(src)

#target_link_libraries(main foo)