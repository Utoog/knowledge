
at: ~/.config/systemd/user/mpd.service
```systemd

[Unit]
Description=Music Player Daemon

[Service]
ExecStart=/usr/bin/mpd --no-daemon

[Install]
WantedBy=default.target

```
