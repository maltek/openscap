add_oscap_test_executable(test_api_seap_concurency "test_api_seap_concurency.c")
target_link_libraries(test_api_seap_concurency ${CMAKE_THREAD_LIBS_INIT})
add_oscap_test_executable(test_api_seap_list "test_api_seap_list.c")
add_oscap_test_executable(test_api_seap_number "test_api_seap_number.c")
add_oscap_test_executable(test_api_seap_spb "test_api_seap_spb.c" "${CMAKE_SOURCE_DIR}/src/OVAL/probes/SEAP/generic/spb.c")
target_include_directories(test_api_seap_spb PUBLIC ${CMAKE_SOURCE_DIR}/src/OVAL/probes/SEAP/generic)
add_oscap_test_executable(test_api_seap_string "test_api_seap_string.c")
add_oscap_test_executable(test_api_SEXP_deepcmp "test_api_SEXP_deepcmp.c")
add_oscap_test_executable(test_api_strto "test_api_strto.c")
target_include_directories(test_api_strto PUBLIC ${CMAKE_SOURCE_DIR}/src/OVAL/probes/SEAP/generic)

add_oscap_test("test_api_seap.sh")
