injector_lib = library(
  'injector',
  files('injector.c'),
  hdrs,
  include_directories: inc,
  vs_module_defs: 'injector.def',
  dependencies: [cc.find_library('dbghelp')],
  install: true,
)
