zxing_sources = [
  'gstzxing.cpp',
  'gstzxingplugin.c',
]
zxing_dep = dependency('zxing', version : '>= 1.1.1', required : get_option('zxing'))
if zxing_dep.found()
	gstzxing = library('gstzxing',
	  zxing_sources,
	  c_args : gst_plugins_bad_args,
	  include_directories : [configinc],
	  dependencies : [gstvideo_dep, zxing_dep],
	  install : true,
	  install_dir : plugins_install_dir,
          override_options : ['cpp_std=c++11'],
	)
	plugins += [gstzxing]
endif
