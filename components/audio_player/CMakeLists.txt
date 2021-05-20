message("Build components/audio_player")
idf_component_register(SRCS "audio_player.c" 
                       INCLUDE_DIRS "include"
					   REQUIRES common audio_renderer web_radio libfaad_decoder fdk-aac_decoder mp3_decoder
					   PRIV_REQUIRES  libm4a fdk-aac libfaad   mad  playlist vector http url_parser fifo controls 
                       )
   
					
set_source_files_properties("libfaad_decoder.c" 
    PROPERTIES COMPILE_FLAGS
  	 -DHAVE_MEMCPY -DSTDC_HEADERS -DHAVE_INTTYPES_H -DHAVE_INTTYPES_H -DHAVE_STRINGS_H -Wno-unused-variable -Wno-unused-but-set-variable
)