# Generated from customcompleter.pro.

cmake_minimum_required(VERSION 3.14)
project(customcompleter LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples/widgets/tools/customcompleter")

find_package(Qt6 COMPONENTS Core)
find_package(Qt6 COMPONENTS Gui)
find_package(Qt6 COMPONENTS Widgets)

add_qt_gui_executable(customcompleter
    main.cpp
    mainwindow.cpp mainwindow.h
    textedit.cpp textedit.h
)
target_link_libraries(customcompleter PUBLIC
    Qt::Core
    Qt::Gui
    Qt::Widgets
)


# Resources:
set(customcompleter_resource_files
    "resources/wordlist.txt"
)

qt6_add_resources(customcompleter "customcompleter"
    PREFIX
        "/"
    FILES
        ${customcompleter_resource_files}
)

install(TARGETS customcompleter
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
