
add_definitions(-DLUA_DL_DLOPEN -DLUA_USE_C89 -DLUA_COMPAT_5_1 -DLUA_COMPAT_5_2 -DLUA_USE_LINUX)

include_directories(../lua)

add_library(luajava SHARED luajava.c)

target_link_libraries(
        luajava
        lua
        android
        log
)

