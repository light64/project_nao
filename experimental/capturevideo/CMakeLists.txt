##
# Copyright (C) 2010 Aldebaran Robotics

cmake_minimum_required(VERSION 2.6.4 FATAL_ERROR)
project(capturevideo)
# this lets you find the qibuild cmake frameworl
find_package(qibuild)


# Here, we create an executable named "capturevideo" from the cpp file.
qi_create_bin(capturevideo capturevideo.cpp)

# Here we say that our executable depends on
# - ALCOMMON (main naoqi lib)
# - ALVISION (for vision definitions)
# - OPENCV (display)
#
# It automatically links with the corresponding libraries and make their headers
# available.
qi_use_lib(capturevideo ALCOMMON ALVISION OPENCV2_CORE OPENCV2_HIGHGUI)
