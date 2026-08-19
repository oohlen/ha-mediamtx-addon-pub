# MediaMTX RTSP Server add-on

Simple Home Assistant Supervisor add-on that runs the official
[bluenviron/mediamtx](https://github.com/bluenviron/mediamtx) Docker image
(successor to the abandoned `aler9/rtsp-simple-server`) with a pinned,
currently-valid image tag.

Created because the community add-ons that wrap this project
(`fuatakgun/rtsp_simple_server`, `SebAndBlocks/hass_mediamtx`) are pinned to
the long-removed `v0.17.6` tag and fail to install.

Exposes RTSP on port 8554 (used by the `fuatakgun/eufy_security` integration's
`rtsp_server_address` option) and RTMP on 1935. No extra configuration is
needed — MediaMTX accepts any stream path by default.
