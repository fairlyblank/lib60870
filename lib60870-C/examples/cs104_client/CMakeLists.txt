include_directories(
   .
)

set(example_SRCS
   simple_client.c
)

IF(MSVC)
set_source_files_properties(${example_SRCS}
                                       PROPERTIES LANGUAGE CXX)
ENDIF(MSVC)

add_executable(simple_client
  ${example_SRCS}
)

target_link_libraries(simple_client
    lib60870
)
