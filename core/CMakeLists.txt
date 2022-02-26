# ______________________________________________________
# Hot Reload Library core module CMakeLists.txt file
#
# @file        CMakeLists.txt
# @author      Ahmet İbrahim AKSOY <aaksoy@nettsi.com>
# @date        26.02.2022
#
# @copyright   2022 NETTSI Informatics Technology Inc.
#
# Unauthorized copying of this file, via any medium is strictly prohibited
# Proprietary and confidential
# ______________________________________________________

make_component(
    hrl.core
    TARGET  TYPE STATIC

    TARGET  TYPE STATIC
            COMPILE_OPTIONS -fPIC
            SUFFIX .fpic
            
    TARGET  TYPE SHARED

    ALL_AUTO_SUFFIX
    ALL_WITH_INSTALL
)