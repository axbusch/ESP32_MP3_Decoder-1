message("Build components/mp3_decoder")
idf_component_register(SRCS "mp3_decoder.c" "../common/common_buffer.c"
                       INCLUDE_DIRS "include"
					   REQUIRES common
					   PRIV_REQUIRES  audio_player audio_renderer  fifo mad
                       ) 
   
   set_property(TARGET ${COMPONENT_LIB} APPEND PROPERTY LINK_INTERFACE_MULTIPLICITY 4)		
