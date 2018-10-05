package(default_visibility = ["//src:socketio"])

cc_library(
  name = "sio_client_impl",
  hdrs = ["sio_client_impl.h"],
  srcs = ["sio_client_impl.cpp"],
  deps = [
    ":sio_packet",
		"//src:sio_client_h",
    "@boost//:asio",
    "@boost//:version",
    "@websocketpp//:websocketpp"
  ]
)

cc_library(
  name = "sio_packet",
  hdrs = ["sio_packet.h"],
  srcs = ["sio_packet.cpp"],
  deps = [
    "//src:sio_message_h",
    "@boost//:lexical_cast",
    "@rapidjson//:rapidjson",
  ]
)