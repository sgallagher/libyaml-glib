g_ir_compiler = find_program('g-ir-compiler')

yaml_glib_deps = [ glib, gobject, gmodule, yaml ]

yaml_glib_sources = [
    'libyaml-glib.vala',
    'error.vala',
    'buildable.vala',
    'builder.vala',
    'loader.vala',
    'writer.vala'
]

yaml_glib_nsversion = 'Yaml-' + NSVERSION

yaml_glib_lib = library(
    'yaml-glib',
    sources : yaml_glib_sources,
    dependencies : yaml_glib_deps,
    soversion: '1.0.0',
    vala_args: '--target-glib=2.58',
    install: true,
    install_dir: [true, true, true]
)

install_data(
    'yaml-0.1.vapi',
    install_dir : 'share/vala/vapi/'
)
