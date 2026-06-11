project('foshud', ['c', 'cpp'],
  version : '0.1',
  default_options : [
    'warning_level=3', 
    'cpp_std=c++17'
  ])

glfw_dep = dependency('glfw3')

glad_dir = include_directories('glad/include')

glad_src = files('glad/src/glad.c') 

freetype_dep = dependency('freetype2', required : true)

glad_dep = declare_dependency(
  include_directories: glad_dir,
  sources: glad_src,
  dependencies: freetype_dep,
)

executable('foshud',
  'main.cpp',
  dependencies : [glad_dep, glfw_dep]
)