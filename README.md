# go2rtc add-on

Runs the official [AlexxIT/go2rtc](https://github.com/AlexxIT/go2rtc) media
server Docker image with a pinned, currently-valid tag.

The `fuatakgun/eufy_security` Home Assistant integration's P2P streamer
(`p2p_streamer.py`) talks directly to go2rtc's REST API on port 1984
(`GO2RTC_API_PORT`) to create a stream and push raw P2P video bytes into it,
then Home Assistant's `stream` component reads the result back via RTSP on
port 8554 (`GO2RTC_RTSP_PORT`). A generic RTSP server (e.g. MediaMTX) does
**not** work for this integration — it specifically requires go2rtc's HTTP
push API.

Set the integration's `rtsp_server_address` option to `127.0.0.1`.
