project(minizip C)

set(ZLIB_MINIZIP_SRC
	ioapi.c
	mztools.c
	unzip.c
	zip.c)

add_library(minizip STATIC ${ZLIB_MINIZIP_SRC})

<<<<<<< Updated upstream
target_link_libraries(minizip PUBLIC zlib)
=======
target_include_directories(minizip PUBLIC . ../../)
target_link_libraries(minizip PUBLIC zlibstatic)
>>>>>>> Stashed changes

install(TARGETS minizip
		ARCHIVE DESTINATION lib)
install(FILES 
	crypt.h
	ioapi.h
	iowin32.h
	mztools.h
	unzip.h
	zip.h
	DESTINATION include)