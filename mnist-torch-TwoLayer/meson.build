project('libtorch-mnist', 'cpp', default_options : ['default_library=static', 'cpp_std=c++14'])

incdir = include_directories('./include', './include/torch/csrc/api/include')

cpp = meson.get_compiler('cpp')
torch_dep = cpp.find_library('torch', dirs: '/mnt/workspace/libtorch_lib')
c10_dep = cpp.find_library('c10', dirs: '/mnt/workspace/libtorch_lib')
protobuf_dep = cpp.find_library('protobuf', dirs: '/mnt/workspace/libtorch_lib')
torch_cpu_dep = cpp.find_library('torch_cpu', dirs: '/mnt/workspace/libtorch_lib')

deps = [torch_dep, torch_cpu_dep, c10_dep, protobuf_dep]
link_flags = ['-lpthread', '-lunwind' ] 

executable('mnist', 'mnist.cpp', include_directories: incdir, dependencies: deps, link_args: link_flags)


