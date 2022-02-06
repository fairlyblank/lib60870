include_directories(
   .
)

set(example_SRCS
   multi_client_server.c
)

IF(MSVC)
set_source_files_properties(${example_SRCS}
                                       PROPERTIES LANGUAGE CXX)
ENDIF(MSVC)

add_executable(multi_client_server
  ${example_SRCS}
)

target_link_libraries(multi_client_server
    lib60870
)
