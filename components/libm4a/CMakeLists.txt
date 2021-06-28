message("Build components/libfaad")
idf_component_register(SRCS "demux.c" "m4a.c"
                       INCLUDE_DIRS "include" 
					   REQUIRES common
                       )

target_compile_options(${COMPONENT_LIB} PRIVATE  -DROCKBOX_LITTLE_ENDIAN
	-Wno-int-conversion
)
					

