project(libelfin-dwarf)

file(GLOB libelfin-dwarf_SRC ${PROJECT_SOURCE_DIR}/*.cc)

add_custom_command(
        OUTPUT            ${PROJECT_SOURCE_DIR}/to_string.cc
        COMMAND           make to_string.cc
        WORKING_DIRECTORY ${PROJECT_SOURCE_DIR}
)

add_library(libelfin-dwarf ${libelfin-dwarf_SRC} ${PROJECT_SOURCE_DIR}/to_string.cc)
target_include_directories(libelfin-dwarf PUBLIC ${PROJECT_SOURCE_DIR})

# dwarf lib depends on elf lib
target_link_libraries(libelfin-dwarf PUBLIC libelfin-elf)
