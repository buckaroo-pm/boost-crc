load('//:buckaroo_macros.bzl', 'buckaroo_deps')

prebuilt_cxx_library(
  name = 'crc', 
  header_only = True, 
  header_namespace = 'boost', 
  exported_headers = subdir_glob([
    ('include/boost', '**/*.hpp'), 
  ]), 
  deps = buckaroo_deps(), 
  visibility = [
    'PUBLIC', 
  ], 
)

cxx_binary(
  name = 'crc-example', 
  srcs = [
    'crc_example.cpp', 
  ], 
  deps = [
    ':crc', 
  ], 
)
