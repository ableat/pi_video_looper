# pi_video_looper
Application to turn your Raspberry Pi into a dedicated looping video playback device, good for art installations, information displays, or just playing cat videos all day.

For best results start with a fresh install of Raspbian. (consider enabling ssh)

```
sudo apt-get update && sudo apt-get install -y git
git clone https://github.com/ableat/pi_video_looper.git
```

Once installed eject the sd card and mount the `/boot` partition on your local machine.

We need to append `config.txt` with the following two lines:
```
display_rotate=3
gpu_mem=256
```
*We need to explicitly set `gpu_mem` otherwise videos won't playback in portrait. This is only required on some pi revisions.*

For more information checkout the [adafruit tutorial](https://learn.adafruit.com/raspberry-pi-video-looper/installation)
