ADD_EXECUTABLE(qtlua_uic qtlua_uic.cc )
QT5_USE_MODULES(qtlua_uic Widgets Core Xml)

IF(MSVC)
	TARGET_LINK_LIBRARIES(qtlua_uic qtlua_static)
ELSE()
	TARGET_LINK_LIBRARIES(qtlua_uic qtlua)
ENDIF()

INSTALL(TARGETS qtlua_uic RUNTIME DESTINATION ${INSTALL_BIN})

