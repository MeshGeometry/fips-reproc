cmake_minimum_required(VERSION 2.8.9)

# include the fips macros
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

set(FIPS_RTTI ON)
set(FIPS_EXCEPTIONS ON)

set (CMAKE_CXX_STANDARD 17)

set(REPROCXX 1)
fips_setup()
fips_project(reproc)
fips_add_subdirectory(reproc)
fips_finish()