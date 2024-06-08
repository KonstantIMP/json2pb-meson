project(
    'json2pb'
    , ['cpp']
    , version: '1.0.0'
    , default_options: 'cpp_std=c++20'
)

json2pb_includes = include_directories('./include/')
json2pb_sources = [
    'source/json2pb.cc'
]
json2pb_dependencies = [
    dependency('protobuf')
    , dependency('jansson')
]

json2pb_lib = shared_library(
    'json2pb'
    , json2pb_sources
    , include_directories: json2pb_includes
    , dependencies: json2pb_dependencies
)

json2pb = declare_dependency(
    link_with: json2pb_lib
    , include_directories: json2pb_includes
)
