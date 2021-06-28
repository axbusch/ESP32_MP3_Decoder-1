message("Build components/audio_player")
idf_component_register(SRCS "audio_player.c" 
                       INCLUDE_DIRS "include"
					   REQUIRES  common audio_renderer mp3_decoder fdk_aac_decoder libfaad_decoder  
					   PRIV_REQUIRES fifo controls   
                       )
   
			
