aux_source_directory(. SRCS)

# add static library
add_library(mylib ${SRCS})

# or add static library
# add_library(mylib SHARED ${SRCS})

install(TARGETS mylib DESTINATION lib)

# for develop
# install(FILES foo.h DESTINATION include)
