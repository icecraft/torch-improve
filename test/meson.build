
project('libtorch-mnist', 'cpp', default_options : ['default_library=static', 'cpp_std=c++14'])

incdir = include_directories('/opt/data/libtorch/include', '/opt/data/libtorch/include/torch/csrc/api/include')

cpp = meson.get_compiler('cpp')
torch_dep = cpp.find_library('torch', dirs: '/home/ares/Git/pytorch/bazel-bin')
c10_dep = cpp.find_library('c10', dirs: '/home/ares/Git/pytorch/bazel-bin')
protobuf_dep = cpp.find_library('protobuf', dirs: '/home/ares/Git/pytorch/bazel-bin/external/com_google_protobuf')
glog_dep = cpp.find_library('glog', dirs: '/home/ares/Git/pytorch/bazel-bin/external/com_github_glog')
gflags_dep = cpp.find_library('gflags', dirs: '/home/ares/Git/pytorch/bazel-bin/external/com_github_gflags_gflags')


#  torch_cpu_dep = cpp.find_library('torch_cpu', dirs: '/home/ares/Git/pytorch/bazel-bin')


executable('app', 'test.cpp', include_directories: incdir, dependencies: [torch_dep, c10_dep, protobuf_dep, glog_dep, gflags_dep])


