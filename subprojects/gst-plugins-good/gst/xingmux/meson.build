xing_sources = [
  'plugin.c',
  'gstxingmux.c',
]

gstxingmux = library('gstxingmux',
  xing_sources,
  c_args : gst_plugins_good_args,
  include_directories : [configinc],
  dependencies : [gstbase_dep],
  install : true,
  install_dir : plugins_install_dir,
)
plugins += [gstxingmux]
