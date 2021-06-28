message("Build components/libfaad_decoder")
idf_component_register(SRCS "libfaad_decoder.c" "../libm4a/m4a.c" "../libm4a/demux.c"
                       INCLUDE_DIRS "include"
					   PRIV_REQUIRES common libfaad libm4a audio_renderer audio_player fifo
)

#set_source_files_properties("libfaad_decoder.c" 
#    PROPERTIES COMPILE_FLAGS
#  	 -DHAVE_MEMCPY -DSTDC_HEADERS -DHAVE_INTTYPES_H -DHAVE_INTTYPES_H -DHAVE_STRINGS_H -Wno-unused-variable -Wno-unused-but-set-variable
#)

target_compile_options(${COMPONENT_LIB} PRIVATE  -DHAVE_MEMCPY -DSTDC_HEADERS -DHAVE_INTTYPES_H 
	-DHAVE_INTTYPES_H -DHAVE_STRINGS_H 
	-Wno-unused-variable -Wno-unused-but-set-variable
)
