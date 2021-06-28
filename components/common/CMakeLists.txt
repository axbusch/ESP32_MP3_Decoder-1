message("Build components/common")
idf_component_register(SRCS "common_buffer.c" 
                       INCLUDE_DIRS "include"
					   REQUIRES fifo
                       )
   
					