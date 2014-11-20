android_aosp
=============
Android Development Environment using Ubuntu 14.04 Base capable of build AOSP

Contains:

    OpenJDK 1.7.0
    Oracle Java JDK 6
    Android SDK r23.0.2
    Android NDK r10c 64/32-bit
    Apache Ant 1.8.4
    Android 5.0 SDK Platform
    Android 4.4.2 SDK
    Support repositories and libraries

Pull from gmetal/android_aosp: docker pull gmetal/android_aosp

Run it with: docker run -i -v /path/to/local/copy/of/aosp/source/code:/usr/local/aosp:rw -t gmetal/android_aosp /bin/bash

You can initialise the AOSP repo and download everything you need from inside the container (e.g. repo init && repo sync)
but because the source code is quite large and will not fit in the docker image, it is best if you store it in
a local path.

Navigate to /usr/local/aosp, and you can initiate the build process: 
source build/envsetup.sh
lunch

etc...

Based on gmetal/android_ndk64 image. 
