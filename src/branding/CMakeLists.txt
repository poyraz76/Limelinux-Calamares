set( COMPONENT_NAME "pisi" )

if( IS_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/lang" )
    add_subdirectory( lang )
endif()

file( GLOB SUBDIRECTORIES RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "*" )
foreach( SUBDIRECTORY ${SUBDIRECTORIES} )
    if( IS_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/${SUBDIRECTORY}" )
        calamares_add_branding_subdirectory( ${SUBDIRECTORY} )
    endif()
endforeach()
