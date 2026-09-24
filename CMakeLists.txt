cmake_minimum_required(VERSION 3.14)
project(noownContainers C)

add_library(noownContainers STATIC
    hashArray/pvd_realization.c
    pVoidArray/pVoidArray.c
)

target_compile_features(noownContainers PUBLIC c_std_99)
target_include_directories(noownContainers PUBLIC
	${CMAKE_CURRENT_SOURCE_DIR}/pVoidArray/
	${CMAKE_CURRENT_SOURCE_DIR}/hashArray/
)
