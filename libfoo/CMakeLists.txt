# Standard CMake prelude - nothing special
cmake_minimum_required(VERSION 3.0)
project(LibFoo C)

add_library(foo STATIC foo.c)

# Here is not-so-standard element.
# The target installation command has to exist
# and has to install all linkable targets 
# into `.` (current) directory for cargo to find it.  
install(TARGETS foo DESTINATION .)
