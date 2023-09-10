include(FetchContent)

FetchContent_Declare(
  googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG        v1.14.0
)
FetchContent_MakeAvailable(googletest)
add_library(GTest::GTest INTERFACE IMPORTED)
target_link_libraries(GTest::GTest INTERFACE gtest_main)

file(GLOB TEST_SOURCE *.cpp)

add_executable(myTest ${TEST_SOURCE})

target_link_libraries(myTest
 PRIVATE
  GTest::GTest
  iodata
  btdconv)

add_test(gtests myTest)
