# play_docker_nginx_rtmp_hls


# Run docker image

```docker
docker run -d -p 1935:1935 -p 8080:8080  alqutami/rtmp-hls
```

# Configure OBS to stream content:


- Go to Settings > Stream, choose the following settings:
    - Service: Custom Streaming Server.
    - Server: rtmp://localhost:1935/live.
    - Stream key: anything you want, however provided video players assume stream key is `test`


# Testing

- Using VLC
    - Go to Media > Open Network Stream.
    - http://localhost:8080/hls/test.m3u8
- [https://videojs.github.io/videojs-contrib-hls/](https://videojs.github.io/videojs-contrib-hls/)
    - http://localhost:8080/hls/test.m3u8
    - Press Load button


# References

[https://hub.docker.com/r/alqutami/rtmp-hls](https://hub.docker.com/r/alqutami/rtmp-hls)

