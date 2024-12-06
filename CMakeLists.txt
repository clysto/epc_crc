cmake_minimum_required(VERSION 3.15)

project(epc_crc VERSION 1.0 LANGUAGES CXX C)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(pybind11 REQUIRED)

pybind11_add_module(epc_crc
    crc.cpp
    crc.hpp
    crc5epc_c1g2.c
    crc5epc_c1g2.h
    crc16genibus.c
    crc16genibus.h
)
