cmake_minimum_required ( VERSION 3.1.0...4.0.0 )
project ( RTWeekend LANGUAGES CXX )

# Set to C++11
set ( CMAKE_CXX_STANDARD          11 )
set ( CMAKE_CXX_STANDARD_REQUIRED ON )
set ( CMAKE_CXX_EXTENSIONS        OFF )

# Source
set ( EXTERNAL 
  src/external/stb_image.h
)

set ( SOURCE_ONE_WEEKEND
  src/InOneWeekend/main.cc
)

include_directories(src)

# GNU compiler
add_compile_options(-Wnon-virtual-dtor)
add_compile_options(-Wreorder)
add_compile_options(-Wmaybe-uninitialized)
add_compile_options(-Wunused-variable)

# Executables
add_executable(inOneWeekend ${EXTERNAL} ${SOURCE_ONE_WEEKEND})
