cmake_minimum_required(VERSION 3.12)
#project(pi_project_test)

set(this PIprojectTests)

set(Sources
        MVPTestes.cpp
    )

include_directories(../PIproject)

add_executable(${this} ${Sources})

target_link_libraries(${this} PUBLIC
        gtest
        gtest_main
		opencv
        )

add_test(
        NAME ${this}
        COMMAND ${this}
)



