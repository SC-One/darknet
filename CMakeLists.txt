set(SUB_PRJ_NAME DarkNet)
if(UNIX)
    if(APPLE)
        add_custom_target(${SUB_PRJ_NAME}
            COMMAND make
            WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
        )
    else()
        add_custom_target(${SUB_PRJ_NAME}
            COMMAND make
            WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
        )
    endif()
else()
    add_custom_target(${SUB_PRJ_NAME}
        COMMAND mingw32-make -f Makefile
        WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
    )
endif()

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
