hdrs_priv = files('injector_internal.h')

injector_lib = library(
  'injector',
  files(
    'elf.c',
    'injector.c',
    'ptrace.c',
    'remote_call.c',
    'shellcode.S',
    'util.c',
  ),
  hdrs,
  hdrs_priv,
  c_args: ['-D_GNU_SOURCE'],
  include_directories: inc,
  install: true,
)
