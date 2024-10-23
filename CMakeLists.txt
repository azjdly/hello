# CMakeLists.txt
cmake_minimum_required(VERSION 3.5)
project(mytest)
set(CMAKE_C_STANDARD 99)



aux_source_directory(${PROJECT_SOURCE_DIR}/src SRC_LIST)

add_executable(
    myhello
    ${SRC_LIST}
)

target_link_directories(myhello PUBLIC
                        ${PROJECT_SOURCE_DIR}/include
)
