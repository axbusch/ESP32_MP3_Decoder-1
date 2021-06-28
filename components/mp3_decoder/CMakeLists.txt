message("Build components/mp3_decoder")
idf_component_register(SRCS "." 
                       INCLUDE_DIRS "include"
					   PRIV_REQUIRES common audio_player audio_renderer  fifo 
                       ) 
   
					