cmake_minimum_required(VERSION 3.5.1)
project(webserver)

set(CMAKE_CXX_STANDARD 14)

add_executable(webserver main.cpp  log/log.cpp  CGImysql/sql_connection_pool.cpp   http/http_conn.cpp  timer/lst_timer.cpp  config.cpp  webserver.cpp )
TARGET_LINK_LIBRARIES(webserver -lpthread -lmysqlclient)
