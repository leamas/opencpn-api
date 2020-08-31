OpenCPN API distribution README
===============================

This repository contains API definitions to be used in plugin
development for [OpenCPN](https://github.com/OpenCPN/OpenCPN)

Each directory contains a complete API definition, including a
CMakeLists.txt. Usage:

  - First copy the api to use to someplace in the plugins, typically
    a directory called libs. Using api-16 i. e. 1.16 from 5.0 this
    creates a directory called *libs/api-16*

  - Use the API by including these lines in main CMakeLists.txt:

        add_subdirectory("libs/api-16")
        target_link_libraries(${PACKAGE_NAME} ocpn::api)


This sets all required header files, libraries and possible compiler
options required by the API.

