cmake_minimum_required(VERSION 3.8)
include_directories("${PROJECT_SOURCE_DIR}/packages/YARA.OpenSSL.x86.1.1.0/include")


set(libcrypto ${PROJECT_SOURCE_DIR}/packages/YARA.OpenSSL.x86.1.1.0/lib/libcrypto.lib)
set(libssl ${PROJECT_SOURCE_DIR}/packages/YARA.OpenSSL.x86.1.1.0/lib/libssl.lib)
add_executable(Demo test.cpp)

target_link_libraries(Demo ${libcrypto} ${libssl})