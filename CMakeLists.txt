#
# CMakeLists.txt
#
#  Created on: 06/giu/2014
#      Author: Luca Muratore (luca.muratore@iit.it)
#

project(sctp_basic_example)

# minimum cmake version required
cmake_minimum_required(VERSION 2.8.7)

# set up our program
add_executable(sctp_server sctp_server.c)
add_executable(sctp_client sctp_client.c)
add_executable(tcp_server tcp_server.c)
add_executable(tcp_client tcp_client.c)

#link lib
target_link_libraries(sctp_server sctp)
target_link_libraries(sctp_client sctp)

install(TARGETS sctp_server sctp_client tcp_server tcp_client DESTINATION bin)
