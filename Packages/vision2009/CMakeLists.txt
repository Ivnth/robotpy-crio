
# regenerate cpp files when sip files change
file(GLOB_RECURSE WPILIB_SIP_SOURCE sip/*.sip)
set(SIP_EXTRA_FILES_DEPEND ${WPILIB_SIP_SOURCE})

ADD_SIP_PYTHON_MODULE(_vision2009 sip/vision2009mod.sip)
set(SIP_EXTRA_FILES_DEPEND)

install(FILES vision2009.py DESTINATION "${ROBOTPY_DEST_SITE_PACKAGES}")