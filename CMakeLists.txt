##---------------------------------------------------------------------------
## Author:      Sean D'Epagnier
## Copyright:   
## License:     GPLv3+
##---------------------------------------------------------------------------
 
# define minimum cmake version
CMAKE_MINIMUM_REQUIRED(VERSION 2.6.2)

PROJECT(messagescope_pi)
SET(PACKAGE_NAME messagescope_pi)
SET(VERBOSE_NAME MessageScope)
SET(TITLE_NAME MessageScope)
SET(CPACK_PACKAGE_CONTACT "Sean D'Epagnier ")

MESSAGE (STATUS "*** Building ${PACKAGE_NAME} ***")

SET(VERSION_MAJOR "0")
SET(VERSION_MINOR "1")

INCLUDE("cmake/PluginConfigure.cmake")

SET(SRC_MESSAGESCOPE
            src/messagescope_pi.cpp
            src/MessageScopeDialog.cpp
            src/MessageScopeUI.cpp
            src/icons.cpp
	    )

ADD_LIBRARY(${PACKAGE_NAME} SHARED ${SRC_MESSAGESCOPE} )

INCLUDE("cmake/PluginInstall.cmake")
INCLUDE("cmake/PluginLocalization.cmake")
INCLUDE("cmake/PluginPackage.cmake")
