set(source_files)

set(test_files)

add_library(algorithm ${source_files})

target_include_directories(algorithm PUBLIC ./include)

add_executable(test_algorithm ${source_files} ${test_files})

target_link_libraries(test_algorithm Catch2::Catch2)
target_link_libraries(test_algorithm algorithm)
