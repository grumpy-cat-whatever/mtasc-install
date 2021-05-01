# Instructions
 1. Compile zlib from source (statically linked)
    1) Downloaded latest version from https://zlib.net/
    2) Extract into a convenient folder (e.g. the user's home directory)
    3) Run the contained `configure` script
    4) Run `make`
    5) **DO NOT** run *make install*, that's not what you're doing this for
 2. Put `zlib.h`, `zconf.h` and `libz.a` (or `libz.lib`) into this folder
    1) *zconf.h* may or may not be necessary; I just did what my predecessors did
