cmake_minimum_required(VERSION 3.0)

PROJECT(hellocmake C)
ADD_DEFINITIONS(-Os -ggdb -Wall -Werror --std=gnu99 -Wmissing-declarations)

SET(CMAKE_SHARED_LIBRARY_LINK_C_FLAGS "")

ADD_EXECUTABLE(hellocmake main.c)

INSTALL(TARGETS hellocmake RUNTIME DESTINATION bin)
