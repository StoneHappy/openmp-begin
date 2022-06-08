find_package(OpenMP REQUIRED)

if(OpenMP_FOUND)
    target_link_libraries(${you_executable_name} OpenMP::OpenMP_CXX)
else()
    message(FATAL_ERROR "openmp not found!")
endif()

add_subdirectory(Vendors)
add_subdirectory(Runtime)
add_subdirectory(App)