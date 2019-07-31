
add_definitions(-DLUA_DL_DLOPEN -DLUA_USE_C89 -DLUA_COMPAT_5_1 -DLUA_COMPAT_5_2 -DLUA_USE_LINUX)

aux_source_directory(. DIR_LUAJ_SRCS)

add_library(luaj luajava.c)

