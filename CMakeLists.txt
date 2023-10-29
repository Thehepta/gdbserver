cmake_minimum_required(VERSION 3.23)
project(linux_proxy)

set(CMAKE_CXX_STANDARD 14)

#find_package(event REQUIRED)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fPIE")
#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIE")
#set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -masm=intel")

#add_executable(gdbinject gdbserver.c signals.c packets.c utils.c gdb/signals.def)
add_executable(gdbinject gdbinject.c signals.c packets.c utils.c gdb/signals.def )

#target_link_libraries(linux_proxy event)
