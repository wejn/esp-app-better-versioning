idf_component_register(SRCS "hello_world_main.c"
                       PRIV_REQUIRES spi_flash
                       INCLUDE_DIRS "")

# Define `BUILD_FULL_REV` to be used in the source
add_definitions(-DBUILD_FULL_REV="${BUILD_TIMESTAMP}-${GIT_FULL_REV_ID}")
