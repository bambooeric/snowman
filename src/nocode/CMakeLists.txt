set(SOURCES
    main.cpp
)

add_executable(nocode ${SOURCES})
<<<<<<< HEAD
target_link_libraries(nocode nc-core ${Boost_LIBRARIES} ${QT_LIBRARIES} ${CMAKE_DL_LIBS})
=======
target_link_libraries(nocode nc ${Boost_LIBRARIES} ${QT_LIBRARIES})
>>>>>>> cd9edcddf873fc40d7bcb1bb1eae815faedd3a03

if (NOT ${IDA_PLUGIN_ENABLED})
    install(TARGETS nocode RUNTIME DESTINATION bin)
    if(WIN32 AND NOT ${NC_QT5})
        install_qt4_executable("bin/nocode.exe")
    endif()
endif()

# vim:set et sts=4 sw=4 nospell:
