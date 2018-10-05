package_group(
  name = "socketio",
  packages = [
    "//src/...",
    "//src/internal/...",
  ]
)

package(default_visibility = ["//src:socketio"])

cc_library(
  name = "sio_client",
  visibility = ["//visibility:public"],
  srcs = [
    "sio_client.cpp",
		"sio_socket.cpp",
  ],
  deps = [
	  ":sio_client_h",
		":sio_message_h",
		":sio_socket_h",
    "//src/internal:sio_client_impl",
		"//src/internal:sio_packet",
  ],
	alwayslink = 1,
)

cc_library(
  name = "sio_client_h",
	hdrs = ["sio_client.h"],
	deps = [
	  ":sio_message_h",
		":sio_socket_h",
	]
)

cc_library(
  name = "sio_message_h",
	hdrs = ["sio_message.h"],
)

cc_library(
  name = "sio_socket_h",
	hdrs = ["sio_socket.h"],
	deps = [
	  ":sio_message_h",
	]
)