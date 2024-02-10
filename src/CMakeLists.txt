add_library(Adafruit_Floppy INTERFACE)

target_compile_definitions(Adafruit_Floppy INTERFACE
    ARDUINO_ARCH_RP2040
)

target_sources(Adafruit_Floppy INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/Adafruit_Floppy.cpp
    ${CMAKE_CURRENT_LIST_DIR}/Adafruit_Floppy.h
    ${CMAKE_CURRENT_LIST_DIR}/Adafruit_MFM_Floppy.cpp
    ${CMAKE_CURRENT_LIST_DIR}/arch_rp2.cpp
    ${CMAKE_CURRENT_LIST_DIR}/arch_rp2.h
    ${CMAKE_CURRENT_LIST_DIR}/greasepack.h
    ${CMAKE_CURRENT_LIST_DIR}/mfm_impl.h
)

target_include_directories(Adafruit_Floppy INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}
)
