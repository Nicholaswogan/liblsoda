cmake_minimum_required(VERSION 3.12)

project(liblsoda LANGUAGES C)
add_library(lsoda
src/cfode.c 
src/cfode_static.c 
src/common.c 
src/corfailure.c 
src/correction.c 
src/daxpy.c 
src/ddot.c 
src/dgefa.c 
src/dgesl.c 
src/dscal.c 
src/fnorm.c 
src/idamax.c 
src/intdy.c 
src/lsoda.c 
src/methodswitch.c 
src/orderswitch.c 
src/prja.c 
src/scaleh.c 
src/solsy.c 
src/stoda.c 
src/vmnorm.c 
src/strdup_printf.c
)
target_include_directories(lsoda PUBLIC src/)

add_executable(test test/test.c)
target_link_libraries(test lsoda)