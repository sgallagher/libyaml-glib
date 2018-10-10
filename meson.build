project('yaml-glib', ['c', 'vala'],        version: '0.2.0',
  meson_version: '>= 0.45.0',
)

NSVERSION = '1.0'

add_project_arguments([
                       '--vapidir',
                       join_paths(meson.current_source_dir(), 'src')
                      ],
                      language: 'vala')

gnome = import('gnome')
pkg = import('pkgconfig')

glib = dependency('glib-2.0', version : '>=2.32')
gobject = dependency('gobject-2.0', version : '>=2.32')
gmodule = dependency('gmodule-2.0', version : '>=2.32')
gtkdoc = dependency('gtk-doc')

yaml = dependency('yaml-0.1', version : '>=0.1.2')

subdir('src')
#subdir('tests')

pkg.generate(
    libraries : yaml_glib_lib,
    version : meson.project_version(),
    name : meson.project_name(),
    filebase : meson.project_name() + '.' + NSVERSION,
    description : 'Module metadata manipulation library',
    requires: [ 'glib-2.0', 'gobject-2.0' ],
)
