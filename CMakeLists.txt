cmake_minimum_required(VERSION 3.26)

project(test_spdlog_with_submodules LANGUAGES CXX)

add_subdirectory(thirdparty/spdlog)

add_executable(test_spdlog_with_submodules
    
    main.cpp
    
)

target_compile_features(test_spdlog_with_submodules PUBLIC cxx_std_23)
target_link_libraries(test_spdlog_with_submodules PUBLIC spdlog::spdlog)