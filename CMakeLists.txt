cmake_minimum_required(VERSION 3.0.0)
project(HW VERSION 0.1.0)

set(SOURCES #добавил файл сорсов
    ExternalClass/Sources/MyClass.cpp
)
#

add_executable(HW main.cpp ${SOURCES})
#
target_include_directories(HW #добавил путь к хедерам
    PRIVATE
    ${PROJECT_SOURCE_DIR}/ExternalClass/Headers
   )
#
set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
