
### Play with prefix lib name
set_target_properties(mylib PROPERTIES PREFIX "")     # -------> No prefix

### Output path for the lib
set(LIBRARY_OUTPUT_PATH "../../../bin/plugins/")

### installing files (whatever the format)
install(
  FILES
  ../js/toto.js
  ../js/tata.js
  DESTINATION
  ../bin/scripts/
)
