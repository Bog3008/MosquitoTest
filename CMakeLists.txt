cmake_minimum_required(VERSION 3.23)
project(MosquittoPublisher)

set(CMAKE_CXX_STANDARD 23)


#find_package (mosquitto REQUIRED COMPONENTS CXX_LIB)
include_directories (D:/mos/mosquitto-master/include)
include_directories (D:/mos/mosquitto-master)


add_executable(MosquittoPublisher main.cpp
        )

target_link_libraries(MosquittoPublisher
        #${mosquitto_CXX_LIB}
        D:/mos/mosquitto-master/build/lib/Debug/mosquitto.lib
        )
