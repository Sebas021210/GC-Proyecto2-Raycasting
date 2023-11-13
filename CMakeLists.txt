cmake_minimum_required(VERSION 3.25)
project(GC_Proyecto2_Raycasting)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(SDL2_INCLUDE_DIR "C:/Libs/SDL/include")
set(SDL2_LIB_DIR "C:/Libs/SDL/lib/x64")
set(SDL2_IMAGE_INCLUDE_DIR "C:/Libs/SDL2_image/include")
set(SDL2_IMAGE_LIB_DIR "C:/Libs/SDL2_image/lib/x64")

# Agregar la ruta de inclusión de la biblioteca glm
set(GLM_INCLUDE_DIR "C:/Users/50242/Documents/Universidad/TercerAño/GraficasComputadora/GC-Proyecto2-Raycasting/glm")

# Utiliza GLM_INCLUDE_DIR en lugar de CMAKE_INCLUDE_PATH
include_directories(${SDL2_INCLUDE_DIR} ${SDL2_IMAGE_INCLUDE_DIR} ${GLM_INCLUDE_DIR})
link_directories(${SDL2_LIB_DIR} ${SDL2_IMAGE_LIB_DIR})

add_executable(GC_Proyecto2_Raycasting main.cpp include/constants.h include/FastNoise.h include/isDefined.h include/print.h)
target_link_libraries(GC_Proyecto2_Raycasting SDL2main SDL2 SDL2_image)
