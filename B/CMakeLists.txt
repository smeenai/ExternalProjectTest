cmake_minimum_required(VERSION 3.4.3)
project(ExternalProjectTest NONE)

execute_process(COMMAND sleep 4)
message(STATUS "B configure slept")

add_custom_target(sleep
                  ALL
                  sleep 4
                  COMMAND echo "B build slept")
