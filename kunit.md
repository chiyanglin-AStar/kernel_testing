### Kernel Kunit testing 

ref : [Kunit](https://kunit.dev/development/index.html)


add the following  into defconfig

    CONFIG_KUNIT=y
    CONFIG_DM_KUNIT_TEST=y

compile steps

    make clean

    make mrproper

    make i386_kunit_defconfig

    make -j $(nproc)


