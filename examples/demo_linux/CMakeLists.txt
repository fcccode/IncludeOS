cmake_minimum_required(VERSION 2.8.9)
if (NOT DEFINED ENV{INCLUDEOS_PREFIX})
  set(ENV{INCLUDEOS_PREFIX} /usr/local)
endif()
project (service C CXX)

# Human-readable name of your service
set(SERVICE_NAME "Linux userspace demo")

# Name of your service binary
set(BINARY       "linux_demo")

# Source files to be linked with OS library parts to form bootable image
set(SOURCES
  service.cpp
  )

include($ENV{INCLUDEOS_PREFIX}/includeos/linux.service.cmake)
