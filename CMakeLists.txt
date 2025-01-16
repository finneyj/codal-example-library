project(codal-example-library C CXX)

RECURSIVE_FIND_DIR(INCLUDE_DIRS "./inc" "*.h")
RECURSIVE_FIND_FILE(SOURCE_FILES "./source" "*.c??")

add_library(codal-example-library
    ${SOURCE_FILES}
)

target_include_directories(codal-example-library PUBLIC ${INCLUDE_DIRS} "${CMAKE_CURRENT_BINARY_DIR}/gen/" )
