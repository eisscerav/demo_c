add_executable(test_op test_op.c)
target_link_libraries(test_op myop)
message(STATUS "${PROJECT_SOURCE_DIR}/src")
target_include_directories(test_op
    PRIVATE
        ${PROJECT_SOURCE_DIR}/src
)