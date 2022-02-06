include_directories(
   .
)

set(example_SRCS
   cs104_server_no_threads.c
)

IF(MSVC)
set_source_files_properties(${example_SRCS}
                                       PROPERTIES LANGUAGE CXX)
ENDIF(MSVC)

add_executable(cs104_server_no_threads
  ${example_SRCS}
)

target_link_libraries(cs104_server_no_threads
    lib60870
)
