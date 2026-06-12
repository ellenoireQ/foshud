project('foshud', ['c', 'cpp'],
  version : '0.1',
  default_options : [
    'warning_level=3', 
    'cpp_std=c++20'
  ])

glfw_dep = dependency('glfw3')

utils_dir = include_directories(['glad/include', 'fonts/'])

glad_src = files('glad/src/glad.c') 

freetype_dep = dependency('freetype2', required : true)

utils_dep = declare_dependency(
  include_directories: utils_dir,
  sources: glad_src,
  dependencies: freetype_dep,
)

executable('foshud',
  'main.cpp',
  dependencies : [utils_dep, glfw_dep]
)