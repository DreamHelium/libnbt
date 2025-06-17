project(nbt-glib LANGUAGES C)

find_package(PkgConfig)

pkg_search_module(GLIB REQUIRED glib-2.0)

add_library(nbt-glib SHARED nbt.c nbt.h)

target_link_libraries(nbt-glib PUBLIC ${GLIB_LIBRARIES})
target_include_directories(nbt-glib PUBLIC ${GLIB_INCLUDE_DIRS})