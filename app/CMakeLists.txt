# ______________________________________________________
# Example application project CMakeLists file
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
    hrl.app 
    TARGET  TYPE EXECUTABLE 
            LINK hrl.core
            OUTPUT_NAME hrl.app.example
)
