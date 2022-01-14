set(headers
    TFT_eSPI.h
    font_latin_hiragana_24.h
)

set(sources
    TFT_eSPI.cpp
    font_latin_hiragana_24.cpp
)

set(dependencies
    arduino-esp32
    freertos
    esp_system

    cpputils
    espcpputils
)

idf_component_register(
    INCLUDE_DIRS
        .
    SRCS
        ${headers}
        ${sources}
    REQUIRES
        ${dependencies}
)
