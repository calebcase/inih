project('inih', 'c',
  version : '0.47',
)

libinih_src = [
  'ini.c'
]

libinih_inc = include_directories('.')

libinih = library('inih', libinih_src,
  install : true,
)

install_headers('ini.h', subdir: 'inih')

libinih_pkg = import('pkgconfig')
libinih_pkg.generate(libinih,
  description : 'Simple .INI file parser in C, good for embedded systems.',
)

inih_dep = declare_dependency(
  include_directories : libinih_inc,
  link_with           : libinih,
)
