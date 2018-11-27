cmake_minimum_required(VERSION 2.8)

get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

fips_setup(PROJECT reproc)

fips_begin_lib(reproc)
	fips_include_directories(reproc/include)
    fips_vs_warning_level(3)
    fips_src(reproc/src/reproc RECURSE GROUP)
    fips_src(reproc/src/reproc++ RECURSE GROUP)
fips_end_lib()

fips_finish()