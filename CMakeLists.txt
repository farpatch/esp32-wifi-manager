if(IDF_VERSION_MAJOR GREATER_EQUAL 4)
    idf_component_register(SRC_DIRS src
        REQUIRES log nvs_flash wpa_supplicant lwip
        INCLUDE_DIRS src)
else()
    set(COMPONENT_SRCDIRS src)
    set(COMPONENT_ADD_INCLUDEDIRS src)
    set(COMPONENT_REQUIRES log nvs_flash wpa_supplicant lwip)
    register_component()
endif()
