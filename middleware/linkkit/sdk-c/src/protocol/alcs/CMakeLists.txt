INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR})
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/include)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/include/exports)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/include/imports)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/log)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/system)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/system/facility)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/utils)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/utils/digest)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/infra/utils/misc)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/alcs)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/alcs/)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/coap)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/coap/CoAPPacket)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/coap/client)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/coap/server)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/http)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/http2)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/http2/nghttp2)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/mqtt)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/mqtt/MQTTPacket)
INCLUDE_DIRECTORIES (${PROJECT_SOURCE_DIR}/src/protocol/mqtt/client)

FILE (GLOB src_protocol_alcs_SRCS
    ${PROJECT_SOURCE_DIR}/src/protocol/alcs/*.c
)

ADD_LIBRARY (iot_alcs OBJECT
    ${src_protocol_alcs_SRCS}
    ${EXTRA_C_SOURCES}
)

