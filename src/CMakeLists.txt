add_subdirectory (LibLinear)

include_directories( CMAKE_CURRENT_SOURCE_DIR )

file(GLOB CPP_FILES "*.cpp")
add_library (bing_objectness_core ${CPP_FILES}) 
target_link_libraries (LIBLINEAR)

install (TARGETS bing_objectness_core 
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib
    )
