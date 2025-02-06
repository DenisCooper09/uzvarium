cmake_minimum_required(VERSION 3.10...3.31)

project(uzvarium VERSION 0.1 LANGUAGES C DESCRIPTION "The element of uzvar.")

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_EXTENSIONS ON)

if (MSVC)
    add_compile_options(/W4 /WX)
else ()
    add_compile_options(-Wall -Wextra -Wpedantic -Werror)
endif ()

add_subdirectory(src bin)
