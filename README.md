## Building
For Goyawifi:

    git clone https://github.com/T110-pmOS/android-headers-17
    git clone https://github.com/T110-pmOS/libhybris
    cd libhybris/hybris
    ./autogen.sh
    export EPREFIX=/system
    export PATH1=/system/lib:/system/vendor/lib/
    export CFLAGS="-D_GNU_SOURCE"
    ./configure --with-android-headers=/home/q/android-headers-17
    make -j2
    make install


## Test

    mkdir /system
    mkdir /data
    mount /dev/mmcblk0p15 /system
    mount /dev/mmcblk0p16 /data
    E.g.
    cd ~/libhybris/hybris/tests
    ./test_sensors

You might need to run some tests wih sudo.
