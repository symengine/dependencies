# Binaries

### MinGW-w64 Binary
- MinGW-w64 binary can be downloaded from [here](http://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win64/Personal%20Builds/mingw-builds/4.9.1/threads-posix/seh/x86_64-4.9.1-release-posix-seh-rt_v3-rev1.7z)

### Python patched libraries
To make python-x86_64-w64-mingw32.7z follow the steps below

- Download the win64 files from http://www.lfd.uci.edu/~gohlke/pythonlibs/#libpython and extract them. For eg:
libpython‑2.7.10‑cp27‑none‑win_amd64.whl

- For each version of Python, create directory structure `PythonXX-x64\libs` and copy `libpythonXX.a` file from extracted files from above

- Select the 4 directories and compress using 7zip.

### GMP binaries

- Download `mingw-get` from www.mingw.org and install `MSYS` core packages and `m4`

- Extract the MinGW-w64 binary to `C:\mingw64`

- Add `C:\mingw64\bin` folder to `PATH` and remove `C:\MinGW\bin` from `PATH`

- Start a `MSYS` shell (`C:\MinGW\msys\1.0\msys.bat`)

- Download `GMP` from [here](http://ftp.gnu.org/gnu/gmp/gmp-6.0.0a.tar.bz2) and extract it

- Change directory into the `GMP` folder from `MSYS` shell

- Run `./configure --prefix=C:\gmp --disable-static --enable-shared --enable-cxx --host=x86_64-w64-mingw32`

- Run `make && make install`

- Select the 4 directories in `C:\gmp` and compress using 7zip
