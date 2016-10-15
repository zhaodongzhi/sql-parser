cmake_minimum_required(VERSION 2.8.9)

project(sql_parser)

set(CMAKE_C_COMPILER g++)
add_definitions(--std=c++11 -Wall -ggdb3)

include_directories(./src)
include_directories(./src/parser)
include_directories(./src/sql)

file(GLOB src "src/*.c*")
file(GLOB parser "src/parser/*.c*")
file(GLOB sql "src/sql/*.c*")
file(GLOB example  "example/*.c*")

add_executable(example ${example} ${src} ${parser} ${sql})

