project(Core-Unit-Tests C CXX)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_C_STANDARD 11)
set(BINARY Unit-Tests)

include(FetchContent)
FetchContent_Declare(
        googletest
        # Specify the commit you depend on and update it regularly.
        URL https://github.com/google/googletest/archive/5376968f6948923e2411081fd9372e71a59d8e77.zip
)
FetchContent_MakeAvailable(googletest)

file(GLOB_RECURSE TEST_SOURCES LIST_DIRECTORIES false *.h *.cpp)
set(SOURCES ${TEST_SOURCES})

add_compile_definitions(GTEST_HAS_PTHREAD)

add_executable(${BINARY} ${TEST_SOURCES})
target_link_libraries(${BINARY} PUBLIC gtest_main pthread)
