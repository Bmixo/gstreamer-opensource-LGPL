mp4_sources = [
  'isomp4-plugin.c',
  'gstisomp4element.c',
  'gstrtpxqtdepay.c',
  'qtdemux.c',
  'qtdemux_types.c',
  'qtdemux_dump.c',
  'qtdemux_lang.c',
  'qtdemux_tags.c',
  'qtdemux_tree.c',
  'qtdemux-webvtt.c',
  'gstisoff.c',
  'gstqtmux.c',
  'gstqtmoovrecover.c',
  'atoms.c',
  'atomsrecovery.c',
  'descriptors.c',
  'properties.c',
  'gstqtmuxmap.c'
]

gstisomp4 = library('gstisomp4',
  mp4_sources,
  c_args : gst_plugins_good_args,
  link_args : noseh_link_args,
  include_directories : [configinc, libsinc],
  dependencies : [gst_dep, gstriff_dep, gstaudio_dep, gstvideo_dep,
                  gstrtp_dep, gsttag_dep, gstpbutils_dep, zlib_dep],
  install : true,
  install_dir : plugins_install_dir,
)
plugins += [gstisomp4]

install_data(sources: 'GstQTMux.prs', install_dir: presetdir)

env = environment()
env.prepend('GST_PRESET_PATH', meson.current_source_dir())
meson.add_devenv(env)
