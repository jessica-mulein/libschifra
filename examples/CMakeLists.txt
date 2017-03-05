
add_executable( schifra_bitio_example01 schifra_bitio_example01.cpp )
add_executable( schifra_bitio_example02 schifra_bitio_example02.cpp )
add_executable( schifra_erasure_channel_example01  schifra_erasure_channel_example01.cpp )
add_executable( schifra_erasure_channel_example02 schifra_erasure_channel_example02.cpp )
add_executable( schifra_file_interleaving_example01 schifra_file_interleaving_example01.cpp )
add_executable( schifra_file_interleaving_example02 schifra_file_interleaving_example02.cpp )
add_executable( schifra_file_interleaving_example03 schifra_file_interleaving_example03.cpp )
add_executable( schifra_interleaving_example01 schifra_interleaving_example01.cpp )
add_executable( schifra_interleaving_example02 schifra_interleaving_example02.cpp )
add_executable( schifra_interleaving_example03 schifra_interleaving_example03.cpp )
add_executable( schifra_reed_solomon_example01 schifra_reed_solomon_example01.cpp )
add_executable( schifra_reed_solomon_example02 schifra_reed_solomon_example02.cpp )
add_executable( schifra_reed_solomon_example03 schifra_reed_solomon_example03.cpp )
add_executable( schifra_reed_solomon_example04 schifra_reed_solomon_example04.cpp )
add_executable( schifra_reed_solomon_example05 schifra_reed_solomon_example05.cpp )
add_executable( schifra_reed_solomon_example06 schifra_reed_solomon_example06.cpp )
add_executable( schifra_reed_solomon_example07 schifra_reed_solomon_example07.cpp )
add_executable( schifra_reed_solomon_example08 schifra_reed_solomon_example08.cpp )
add_executable( schifra_reed_solomon_file_decoding_example schifra_reed_solomon_file_decoding_example.cpp )
add_executable( schifra_reed_solomon_file_encoding_example schifra_reed_solomon_file_encoding_example.cpp )
add_executable( schifra_reed_solomon_file_interleaving_example schifra_reed_solomon_file_interleaving_example.cpp )
add_executable( schifra_reed_solomon_gencodec_example schifra_reed_solomon_gencodec_example.cpp )
add_executable( schifra_reed_solomon_product_code_example schifra_reed_solomon_product_code_example.cpp )
message( "THREADING EXAMPLES REQUIRE BOOST")
add_executable( schifra_reed_solomon_threads_example01 schifra_reed_solomon_threads_example01.cpp )
add_executable( schifra_reed_solomon_threads_example02 schifra_reed_solomon_threads_example02.cpp )
install(TARGETS schifra_bitio_example01 schifra_bitio_example02
                schifra_erasure_channel_example01 schifra_erasure_channel_example02
                schifra_file_interleaving_example01 schifra_file_interleaving_example02 schifra_file_interleaving_example03
                schifra_interleaving_example01 schifra_interleaving_example02 schifra_interleaving_example03
                schifra_reed_solomon_example01 schifra_reed_solomon_example02 schifra_reed_solomon_example03 schifra_reed_solomon_example04 schifra_reed_solomon_example05 schifra_reed_solomon_example06 schifra_reed_solomon_example07 schifra_reed_solomon_example08
                schifra_reed_solomon_file_decoding_example schifra_reed_solomon_file_encoding_example schifra_reed_solomon_file_interleaving_example
                schifra_reed_solomon_gencodec_example schifra_reed_solomon_product_code_example
                schifra_reed_solomon_threads_example01 schifra_reed_solomon_threads_example02
              DESTINATION example)
