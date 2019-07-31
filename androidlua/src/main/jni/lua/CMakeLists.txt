
#set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -pie -fPIE")

add_definitions(-DLUA_DL_DLOPEN -DLUA_USE_C89 -DLUA_COMPAT_5_1 -DLUA_COMPAT_5_2 -DLUA_USE_LINUX)

aux_source_directory(. DIR_LUA_SRCS)

add_library(lua ${DIR_LUA_SRCS})
