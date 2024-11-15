### Kernel selftest Steps :

ref: [Linux Kernel Selftests](https://docs.kernel.org/dev-tools/kselftest.html)

sudo apt-get install linux-headers-$(uname -r)

sudo apt-get install linux-headers-6.11.0-9-generic

sudo apt-get install linux-headers-6.11.0-9

cd /usr/src/linux-headers-6.11.0-9-generic/

sudo apt-get install gcc-multilib libc6-i386 libc6-dev-i386


### Kernel 5.5.16 note :

    mlock-random-test.c:8:10: fatal error: sys/capability.h: No such file or directory
    8 | #include <sys/capability.h>

    single_step_syscall.c:58:22: error: variably modified ‘altstack_data’ at file scope
   58 | static unsigned char altstack_data[SIGSTKSZ];


### Kernel 5.16.9 note:
    memfd_secret.c:16:10: fatal error: sys/capability.h: No such file or directory
   16 | #include <sys/capability.h>