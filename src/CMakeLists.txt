set(CMAKE_CXX_STANDARD 20)
cmake_minimum_required(VERSION 3.22)
project(lab57)


add_compile_options(-pthread)

add_executable(client client.cpp tree.cpp)
add_executable(server main.cpp tree.cpp)


# Линковка с библиотекой ZeroMQ
target_link_libraries(client PRIVATE zmq)
target_link_libraries(server PRIVATE zmq)
