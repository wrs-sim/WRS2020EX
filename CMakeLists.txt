if(NOT ENABLE_GUI)
  return()
endif()

if(NOT BUILD_SCENE_EFFECTS_PLUGIN OR NOT BUILD_WRS2018 OR NOT BUILD_HAIRO_WORLD_PLUGIN)
  return()
endif()

if(NOT BUILD_WRS2020)
  return()
endif()

install(DIRECTORY
  project
  share
  DESTINATION ${CHOREONOID_SHARE_SUBDIR}/WRS2020)

add_subdirectory(src)