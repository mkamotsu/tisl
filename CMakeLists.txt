cmake_minimum_required(VERSION 3.30.2)

project(tisl)

set(CMAKE_C_COMPILER "clang")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -lm -O2 -DTISL_C -DTISL_TEST")

add_executable(tisl
    src/tisl/built_in_object.c
    src/tisl/evaluator.c
    src/tisl/gc.c
    src/tisl/object.c src/tisl/object_2.c src/tisl/object_3.c
    src/tisl/operation.c src/tisl/operation_2.c 
    src/tisl/primitive_operation.c
    src/tisl/reader.c src/tisl/tisl.c src/tisl/tni.c
    src/tisl/translator.c src/tisl/translator_1.c
    src/tisl/translator_2.c src/tisl/vm.c src/tisl/writer.c
    src/tisl/c/function.c src/tisl/c/opcode.c
    src/tisl/c/translator_3.c
    src/tisl/interpreter.c
    src/console_app/main.c
)
