hdrs_priv = files('injector_internal.h')

injector_lib = library(
  'injector',
  files(
    'exc_handler.c',
    'injector.c',
    'mach.c',
    'mach_excServer.c',
    'ptrace.c',
    'remote_call.c',
    'util.c',
  ),
  hdrs,
  hdrs_priv,
  include_directories: inc,
  install: true,
)
