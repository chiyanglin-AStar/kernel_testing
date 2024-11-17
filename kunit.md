### Kernel Kunit testing 

ref : 

- [Kunit](https://kunit.dev/development/index.html)

- [KUnit - Linux Kernel Unit Testing](https://docs.kernel.org/dev-tools/kunit/index.html)

- [kernel sources](https://cdn.kernel.org/pub/linux/kernel)

- [Running kunit tests on QEMU¶](https://docs.kernel.org/dev-tools/kunit/run_wrapper.html#kunit-on-qemu)


add the following  into defconfig

    CONFIG_KUNIT=y
    CONFIG_DM_KUNIT_TEST=y

compile steps

    make clean

    make mrproper

    make i386_kunit_defconfig

    make -j $(nproc)

### run kunit steps:

[ref :](https://kunit.dev/usage/index.html) 

Once you have the kunitconfig file, just run:

        ./tools/testing/kunit/kunit.py run

        ./tools/testing/kunit/kunit.py run --timeout=30 --jobs=24 --defconfig
--timeout sets a maximum amount of time to allow tests to run.

--jobs sets the number of threads to use to build the kernel.

--defconfig uses an default kunitconfig in the kernel source.

For more information on these and other flags, try running:

        ./tools/testing/kunit/kunit.py run --help


