add_custom_command(OUTPUT html/index.html
  COMMAND doxygen
  COMMAND rm -rf html
  COMMAND sphinx-build -b html . html
  DEPENDS conf.py index.rst)
add_custom_target(doc DEPENDS html/index.html)
