# RunCPM.cloud
Run CP/M in a Docker container

----

<pre>
RunCPM is an application that can execute vintage CP/M 8-bit programs on many modern platforms,
such as Windows, Mac OS X, Linux, FreeBSD, Arduino DUE, and variants like the Teensy or ESP32.
It can be built both on 32 and 64 bits host environments and should be easily portable to other platforms.
RunCPM is fully written in C in a modular way, so porting to other platforms should only require
writing an abstraction layer file for it. No modification to the main code modules should be necessary.
</pre>
Read the full description on its source: https://github.com/MockbaTheBorg/RunCPM

### Build
`$ BUILD="<arch>"; docker buildx build -t <your_repo>/runcpm:"${BUILD}" -f Dockerfile."${BUILD}" .`
**NOTE**: `<arch> = x86-64|aarch64`

### Run
`$ docker run -it --rm --name RunCPM <your_repo>/runcpm:"${BUILD}"`

