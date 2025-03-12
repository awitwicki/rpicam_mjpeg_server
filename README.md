# rpicam_mjpeg_server
Simple mjpeg server for pi camera using opencv 

## Install

```shell
python3 -m venv flask_env
source flask_env/bin/activate
python3 -m pip install flask opencv-python
```

If errors with camera then try install & update dependencies (and update readme):

```shell
# libcamera-hello
# sudo apt update
# sudo apt upgrade -y
# sudo apt install -y libcap-dev

# python3 -m pip install flask --break-system-packages
# source flask_env/bin/activate
# python3 -m pip install flask opencv-python picamera2
```

## Test

1. `python3 main.py`
2. Open in browser `192.168.1.X:5008/video_feed`

## Setup autostart (service daemon)

```shell
# sudo cp main.service /etc/systemd/system/main.service
# sudo systemctl daemon-reload
# sudo systemctl enable main.service
# sudo systemctl start main.service
# sudo systemctl status main.service
# sudo journalctl -u main.service -f
```

