cmake_minimum_required(VERSION 3.23)
project(MosquittoPublisher)

set(CMAKE_CXX_STANDARD 23)

INCLUDE_DIRECTORIES(E:/mosquitto)
LINK_DIRECTORIES(E:/mosquitto/devel)


#add_library(mosquitto E:/mosquitto/mosquitto.dll)

add_executable(MosquittoPublisher main.cpp
        E:/mosquitto/devel/mosquitto.h
        )

#TARGET_LINK_LIBRARIES(MosquittoPublisher E:/mosquitto/devel/mosquitto.lib)
TARGET_LINK_LIBRARIES(MosquittoPublisher E:/mosquitto/mosquitto.dll)
#target_link_libraries(pthread_task pthread.a libc.a)
#install(TARGETS pthread_task DESTINATION ${CMAKE_INSTALL_PREFIX})