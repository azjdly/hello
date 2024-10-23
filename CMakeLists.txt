# CMakeLists.txt
cmake_minimum_required(VERSION 3.5)
project(mytest)
set(CMAKE_C_STANDARD 99)


set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
aux_source_directory(${PROJECT_SOURCE_DIR}/src SRC_LIST)
message(${PROJECT_SOURCE_DIR})
add_executable(
    myhello
    ${SRC_LIST}
)

target_include_directories(myhello PUBLIC

                        ${PROJECT_SOURCE_DIR}/include
)
