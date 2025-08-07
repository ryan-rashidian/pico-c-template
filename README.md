# RPi Pico-2 W C/C++ SDK project template

## Setup 

- Clone Pico SDK (replace `/path/to/pico-sdk` with preferred path):
```bash
git clone https://github.com/raspberrypi/pico-sdk.git /path/to/pico-sdk
```

- Create my_project/build/ folder and run CMake inside:
```bash
cmake .. -DPICO_SDK_PATH=/path/to/pico-sdk -DPICO_BOARD=pico_w -DCMAKE_EXPORT_COMPILE_COMMANDS=ON
```

- Symlink compile_commands.json to project root:
```bash
ln -sf build/compile_commands.json .
```

