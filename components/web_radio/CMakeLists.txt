message("Build components/web_radio")
idf_component_register(SRCS "web_radio.c" 
                       INCLUDE_DIRS "include"
					   PRIV_REQUIRES vector  url_parser http url_parser controls
					   REQUIRES audio_player playlist )
					  
					   
					