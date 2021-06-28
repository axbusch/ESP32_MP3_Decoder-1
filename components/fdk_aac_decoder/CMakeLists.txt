message("Build components/fdk_aac_decoder")
idf_component_register(SRCS "fdk_aac_decoder.c" 
                       INCLUDE_DIRS "include"
					   REQUIRES  common audio_player fdk-aac libm4a 
					   )
   
					
target_compile_options(${COMPONENT_LIB} PRIVATE   
	-Wno-int-conversion -Wno-unused-variable -Wno-discarded-qualifiers
)
					
					
   set_property(TARGET ${COMPONENT_LIB} APPEND PROPERTY LINK_INTERFACE_MULTIPLICITY 3)		