# Useful binaries for RTS3903N Linux 3.10
`Linux version 3.10.27 (zhangzhidan@XY-201) (gcc version 4.8.5 20150209 (prerelease) (Realtek RSDK-4.8.5p1 Build 2521) ) #29 PREEMPT Wed May 22 14:16:12 CST 2019
`

## Update: 10/10/2021
I've now compiled and included the uClibc 0.9.33 interpreter with LD_PRELOAD enabled (disabled by default on the stock SDK), this is incredibly useful for hooking/trampoling library calls.\
Usage: `mount -o bind ld-uClibc-0.9.33.so /lib/ld-uClibc-0.9.33.so`

Here is a collection of binaries I've compiled while debugging and developing on the RTS3903N chipset.
## What's included
- busybox
- darkhttpd
- dropbear
- ffmpeg
- ffprobe
- ffserver
- gdbserver
- lsof
- netcat
- strace
- socat
- v4l2-ctl
- v4l2grab
- Realtek Specific (controlling hardware and ipcam)
    - dbg_isp (can produce a sample h264 stream)
    - realtek_isp_tuning
    - rts_isp_cmd
    - rts_set_gpio

### Other resources
- Toolchains
    - [rsdk-4.8.5-5281-EL-3.10-u0.9.33-m32fut-161202](https://github.com/cjj25/RTS3903N-rsdk-4.8.5-5281)
    - [rsdk-6.4.1-5281-EL-4.9-u1.0-m32fut-180611](https://github.com/cjj25/RTS3903N-rsdk-4.8.5-5281)
- [RTSPServer](https://github.com/cjj25/Yi-RTS3903N-RTSPServer)

### Interesting research
- https://dalpix.com/reverse-engineering-ip-camera-part-4 @aporto
- https://drmnsamoliu.github.io/ @DrmnSamoLiu
- https://georgeimmi.com/download/tapo/c200/ @DrmnSamoLiu
