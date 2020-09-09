project(libelfin-examples)

add_executable(dump-lines dump-lines.cc)
target_link_libraries(dump-lines libelfin)

add_executable(dump-sections dump-sections.cc)
target_link_libraries(dump-sections libelfin)

add_executable(dump-segments dump-segments.cc)
target_link_libraries(dump-segments libelfin)

add_executable(dump-syms dump-syms.cc)
target_link_libraries(dump-syms libelfin)

add_executable(dump-tree dump-tree.cc)
target_link_libraries(dump-tree libelfin)

add_executable(find-pc find-pc.cc)
target_link_libraries(find-pc libelfin)
