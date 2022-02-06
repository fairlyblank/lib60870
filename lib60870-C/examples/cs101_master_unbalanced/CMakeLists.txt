include_directories(
   .
)

set(example_SRCS
   master_example.c
)

IF(MSVC)
set_source_files_properties(${example_SRCS}
                                       PROPERTIES LANGUAGE CXX)
ENDIF(MSVC)

add_executable(cs101_master_unbalanced
  ${example_SRCS}
)

target_link_libraries(cs101_master_unbalanced
    lib60870
)
