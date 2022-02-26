# ______________________________________________________
# HRL project top level CMakeLists.txt file
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

cmake_minimum_required(VERSION 3.00)

project(HRL VERSION 0.0.1 LANGUAGES CXX)

# Turn on any desired tool/feature below.
SET(HRL_MISC_NO_HADOUKEN_BANNER                       FALSE CACHE BOOL "Enable/disable hadouken banner printing"                      FORCE)
SET(HRL_TOOLCONF_USE_IWYU                             FALSE CACHE BOOL "Enable/disable include what you use integration"              FORCE)
SET(HRL_TOOLCONF_USE_GOOGLE_TEST                      FALSE CACHE BOOL "Enable/disable gtest/gmock integration"                       FORCE)
SET(HRL_TOOLCONF_USE_GOOGLE_BENCH                     FALSE CACHE BOOL "Enable/disable google benchmark integration"                  FORCE)
SET(HRL_TOOLCONF_USE_CLANG_FORMAT                     FALSE CACHE BOOL "Enable/disable clang-format integration"                      FORCE)
SET(HRL_TOOLCONF_USE_CLANG_TIDY                       FALSE CACHE BOOL "Enable/disable clang-tidy integration"                        FORCE)
SET(HRL_TOOLCONF_USE_CPPCHECK                         FALSE CACHE BOOL "Enable/disable cppcheck integration"                          FORCE)
SET(HRL_TOOLCONF_USE_CCACHE                           FALSE CACHE BOOL "Enable/disable ccache integration"                            FORCE)
SET(HRL_TOOLCONF_USE_GCOV                             FALSE CACHE BOOL "Enable/disable gcov integration"                              FORCE)
SET(HRL_TOOLCONF_USE_LLVM_COV                         FALSE CACHE BOOL "Enable/disable llvm-cov integration"                          FORCE)
SET(HRL_TOOLCONF_USE_COVERAGE                         FALSE CACHE BOOL "Enable/disable automatic coverage selection integration"      FORCE)
SET(HRL_TOOLCONF_USE_LCOV                             FALSE CACHE BOOL "Enable/disable lcov integration"                              FORCE)
SET(HRL_TOOLCONF_USE_GCOVR                            FALSE CACHE BOOL "Enable/disable gcovr integration"                             FORCE)
SET(HRL_TOOLCONF_USE_DOXYGEN                          FALSE CACHE BOOL "Enable/disable doxygen integration"                           FORCE)
SET(HRL_DISABLE_UNIT_TEST_TARGETS                     FALSE CACHE BOOL "Enable/disable project-wide unit test target creation"        FORCE)
SET(HRL_DISABLE_BENCHMARK_TARGETS                     FALSE CACHE BOOL "Enable/disable project-wide benchmark target creation"        FORCE)
SET(HRL_DISABLE_STATIC_TARGETS                        FALSE CACHE BOOL "Enable/disable project-wide static library target creation"   FORCE)
SET(HRL_DISABLE_SHARED_TARGETS                        FALSE CACHE BOOL "Enable/disable project-wide benchmark target creation"        FORCE)
SET(HRL_DISABLE_EXECUTABLE_TARGETS                    FALSE CACHE BOOL "Enable/disable project-wide executable target creation"       FORCE)
SET(HRL_DISABLE_INTERFACE_TARGETS                     FALSE CACHE BOOL "Enable/disable project-wide interface target creation"        FORCE)
SET(HRL_HADOUKEN_CONAN_GOOGLE_TEST_PKG_NAME           "gtest"     CACHE STRING "Google unit test tool default package name"           FORCE)
SET(HRL_HADOUKEN_CONAN_GOOGLE_TEST_PKG_VERSION        "1.11.0"    CACHE STRING "Google unit test tool default package version"        FORCE)
SET(HRL_HADOUKEN_CONAN_GOOGLE_BENCHMARK_PKG_NAME      "benchmark" CACHE STRING "Google benchmark tool default package name"           FORCE)
SET(HRL_HADOUKEN_CONAN_GOOGLE_BENCHMARK_PKG_VERSION   "1.5.3"     CACHE STRING "Google benchmark tool default package version"        FORCE)
SET(HRL_HADOUKEN_CONAN_PROFILE_FILE                   ""          CACHE STRING "Conan profile file path"                              FORCE)
# SET(HRL_TOOLCONF_GCOV_PATHS                           "/usr/bin"  CACHE STRING "GCov executable search paths"                         FORCE)
# SET(HRL_TOOLCONF_GCOV_NAMES                           "gcov"      CACHE STRING "GCov executable search names"                         FORCE)


# Include hadouken
include(.hadouken/hadouken.cmake)

# Print VCS status to stdout
hdk_git_print_status()

# Components of the project
add_subdirectory(app)

