cmake_minimum_required(VERSION 3.8)
project(benchmark C CXX)

include_directories(
    ${INFERENCE_SOURCE_DIR}/loadgen
)

link_directories(
    ${LOADGEN_BUILD_DIR}
)

add_executable(benchmark "src/main.cc")

target_link_libraries(benchmark
    android
    log
    mlperf_loadgen
)