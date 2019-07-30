# Sets the minimum version of CMake required to build your native library.
# This ensures that a certain set of CMake features is available to
# your build.

cmake_minimum_required(VERSION 3.4.1)

# Specifies a library name, specifies whether the library is STATIC or
# SHARED, and provides relative paths to the source code. You can
# define multiple libraries by adding multiple add.library() commands,
# and CMake builds them for you. When you build your app, Gradle
# automatically packages shared libraries with your APK.

add_library( # Specifies the name of the library.
        luajava

        # Sets the library as a shared library.
        SHARED

        # Provides a relative path to your source file(s).
        luajava/luajava.c
        lua/lapi.c
        lua/lauxlib.c
        lua/lbaselib.c
        lua/lbitlib.c
        lua/lcode.c
        lua/lcorolib.c
        lua/lctype.c
        lua/ldblib.c
        lua/ldebug.c
        lua/ldo.c
        lua/ldump.c
        lua/lfunc.c
        lua/lgc.c
        lua/linit.c
        lua/liolib.c
        lua/llex.c
        lua/lmathlib.c
        lua/lmem.c
        lua/loadlib.c
        lua/lobject.c
        lua/lopcodes.c
        lua/loslib.c
        lua/lparser.c
        lua/lstate.c
        lua/lstring.c
        lua/lstrlib.c
        lua/ltable.c
        lua/ltablib.c
        lua/ltm.c
        lua/lundump.c
        lua/lutf8lib.c
        lua/lvm.c
        lua/lzio.c

        )


target_include_directories(luajava PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/lua
        ${CMAKE_CURRENT_SOURCE_DIR}/luajava)
message('=======================================================')
message(${CMAKE_CURRENT_SOURCE_DIR}/lua)
target_link_libraries(luajava
        android
        log)
