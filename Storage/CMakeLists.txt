cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
project(Storage LANGUAGES CXX)

include(../build/BuildDefaults.cmake)
find_package(sqlite3 REQUIRED)

add_subdirectory("SQLiteStorage")

