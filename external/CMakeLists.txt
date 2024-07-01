message(WARNING "Enable/uncomment the below line to fix error finding yaml-cpp when included from source.")
# set(CERBERUS_CPP_FIND_YAML_CPP OFF)
add_subdirectory(cerberus-cpp EXCLUDE_FROM_ALL)

add_subdirectory(yaml-cpp EXCLUDE_FROM_ALL)
target_include_directories(yaml-cpp SYSTEM INTERFACE
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/yaml-cpp/include>
)
