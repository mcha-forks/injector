executable(
  'injector',
  files('main.c'),
  ya_getopt_hdrs,
  c_args: ['-D_GNU_SOURCE'],
  dependencies: [injector_dep],
  link_with: cc.has_function('getopt') ? [] : [ya_getopt_lib],
  install: true,
)
