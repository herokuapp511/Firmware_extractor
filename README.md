## Requirements
- protobuf
- LZMA
- 7z
- lz4
### Linux
```
git clone https://github.com/AndroidDumps/Firmware_extractor.git && cd Firmware_extractor && sudo apt update && sudo apt install -y unace unrar zip unzip p7zip-full p7zip-rar sharutils rar uudeview mpack arj cabextract rename liblzma-dev python-pip brotli lz4 protobuf-compiler git gawk && pip install backports.lzma protobuf pycrypto twrpdtgen extract-dtb pycryptodome
```
### Mac
```
brew install protobuf liblzma-dev brotli lz4
pip install backports.lzma protobuf pycrypto twrpdtgen extract-dtb
```
Also install [mono](https://www.mono-project.com/docs/getting-started/install/mac/)

### Windows
Install cygwin, and select

```Latest python and pip packages, arj, brotli, cabextract, dos2unix, lz4, p7zip, renameutils, sharutils, unace, unzip and zip```

If you get syntax errors run dos2unix on extractor.sh


### Misc

- Install rust using https://rustup.rs/
- Run `git clone https://github.com/crazystylus/otadump` , `cd otadump/`, `cargo build --release`.
- Navigate to `/target/release` and add the generated `otadump` executable to your PATH.

## How to use
### Download
```
git clone --recurse-submodules https://github.com/AndroidDumps/Firmware_extractor.git
```

### Extract images from firmware URL
Example: Extracting images from pixel 2 factory image:
```
cd Firmware_extractor
wget https://dl.google.com/dl/android/aosp/walleye-pq3a.190705.001-factory-cc471c8c.zip -o firmware.zip
./extractor.sh firmware.zip
```
output will be on "Firmware_extractor/out"
