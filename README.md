# RPi Pico-2 W C/C++ SDK project template

## Setup 

- Clone Pico SDK (replace `/path/to/pico-sdk` with preferred path):
```bash
git clone https://github.com/raspberrypi/pico-sdk.git /path/to/pico-sdk
cd pico-sdk
git submodule update --init
```

- Create my_project/build/ folder and run CMake inside:
```bash
cmake .. -DPICO_SDK_PATH=/path/to/pico-sdk -DPICO_BOARD=pico2_w -DCMAKE_EXPORT_COMPILE_COMMANDS=ON
```

- Symlink compile_commands.json to project root:
```bash
ln -sf build/compile_commands.json .
```

## Build

```bash
 cmake .. -DPICO_SDK_PATH=/path/to/pico-sdk -DPICO_BOARD=pico2_w -DPICO_PLATFORM=rp2350 -DCMAKE_VERBOSE_MAKEFILE=ON
 make
```
