project(libelfin-elf)

file(GLOB libelfin-elf_SRC ${PROJECT_SOURCE_DIR}/*.cc)

add_custom_command(
        OUTPUT            ${PROJECT_SOURCE_DIR}/to_string.cc
        COMMAND           make to_string.cc
        WORKING_DIRECTORY ${PROJECT_SOURCE_DIR}
)

add_library(libelfin-elf ${libelfin-elf_SRC} ${PROJECT_SOURCE_DIR}/to_string.cc)
target_include_directories(libelfin-elf PUBLIC ${PROJECT_SOURCE_DIR})
