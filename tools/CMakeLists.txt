cmake_minimum_required(VERSION 2.8)

project(marisa)

foreach(cmd
  marisa-build
  marisa-dump
  marisa-benchmark
  marisa-lookup
  marisa-predictive-search
  marisa-reverse-lookup
  marisa-common-prefix-search
  )
  
add_executable(${cmd} ${cmd}.cc cmdopt.cc)
target_link_libraries(${cmd} marisa)
target_include_directories(${cmd} PRIVATE ../include)

endforeach(cmd)

