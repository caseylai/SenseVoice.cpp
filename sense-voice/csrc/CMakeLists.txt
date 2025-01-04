add_subdirectory(third-party/ggml)

set(SOURCE_FILES
        common.h
        common.cc
        sense-voice-frontend.h
        sense-voice-frontend.cc
        fftsg.cc
        log-mel-filter-bank.h
        sense-voice-encoder.h
        sense-voice-encoder.cc
        sense-voice-decoder.h
        sense-voice-decoder.cc
        sense-voice.h
        sense-voice.cc
)

include_directories(third-party/ggml/include)

add_library(sense-voice-core STATIC ${SOURCE_FILES})
target_compile_features(sense-voice-core PRIVATE cxx_std_11)
target_link_libraries(sense-voice-core PRIVATE ggml)