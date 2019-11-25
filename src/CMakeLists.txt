set(libnecpp_SOURCES libNEC.cpp misc.cpp matrix_algebra.cpp electromag.cpp
    c_ggrid.cpp c_geometry.cpp c_evlcom.cpp c_plot_card.cpp
    nec_context.cpp nec_exception.cpp nec_radiation_pattern.cpp nec_results.cpp
    nec_structure_currents.cpp nec_output.cpp nec_ground.cpp)
set(libnecpp_HEADERS libnecpp.h misc.h   matrix_algebra.h   electromag.h
    c_ggrid.h   c_geometry.h   c_evlcom.h   c_plot_card.h
    nec_context.h   nec_exception.h   nec_radiation_pattern.h   nec_results.h
    nec_structure_currents.h   nec_output.h   nec_ground.h
    math_util.h common.h typesave_stdint.h nec_debug.h nec_wire.h)

configure_file("${PROJECT_SOURCE_DIR}/necpp/src/config.h.in"
               "${PROJECT_BINARY_DIR}/necpp/src/config.h" )

add_library(necpp ${libnecpp_SOURCES})

