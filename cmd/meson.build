has_getopt = cc.has_function('getopt') and cc.check_header('getopt.h')

executable(
  'injector',
  files('main.c') + (has_getopt ? ya_getopt_hdrs : []),
  c_args: ['-D_GNU_SOURCE'] + (has_getopt ? ['-DNO_YA_GETOPT'] : []),
  dependencies: [injector_dep],
  link_with: has_getopt ? [] : [ya_getopt_lib],
  install: true,
)
