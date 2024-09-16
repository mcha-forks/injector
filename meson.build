project(
  'injector',
  'c',
  version: '0.1.0',
  # LGPL-2.1-or-later: include/, src/
  # GPL-2.0-or-later: cmd/
  # BSD-2-Clause: util/
  license: 'LGPL-2.1-or-later AND GPL-2.0-or-later AND BSD-2-Clause',
  meson_version: '>=0.56.0',
  default_options: [
    'c_std=c11',
    'b_vscrt=from_buildtype',
  ],
)

cc = meson.get_compiler('c')

inc = include_directories('include')

hdrs = files('include/injector.h')

if host_machine.system() in ['windows', 'cygwin']
  subdir('src/windows')
elif host_machine.system() == 'darwin'
  subdir('src/macos')
elif host_machine.system() == 'linux'
  subdir('src/linux')
endif

install_headers(hdrs)

injector_dep = declare_dependency(
  link_with: injector_lib,
  include_directories: inc,
)

meson.override_dependency('injector', injector_dep)

subdir('util')
subdir('cmd')
