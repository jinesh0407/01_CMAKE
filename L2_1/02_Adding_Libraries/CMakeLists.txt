cmake_minimum_required(VERSION 3.28)
project(OLAS)

add_executable(${PROJECT_NAME} main.cpp)

# To include/add the subdirectory
add_subdirectory(Adder)
# To include the subdirectory HEADER FILE
target_include_directories(${PROJECT_NAME} PUBLIC Adder)      # adder --> Not working
# Where to find the LIBRARIES
target_link_directories(${PROJECT_NAME} PRIVATE adder)        # adder --> working

# To BUILD
target_link_libraries(${PROJECT_NAME} PRIVATE adder)
