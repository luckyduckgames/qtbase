# Generated from benchlibcallgrind.pro.

#####################################################################
## benchlibcallgrind Binary:
#####################################################################

add_qt_executable(benchlibcallgrind
    NO_INSTALL # special case
    OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR} # special case
    SOURCES
        tst_benchlibcallgrind.cpp
    PUBLIC_LIBRARIES
        Qt::Test
)

## Scopes:
#####################################################################
