### Issues

### The reason for the following issue is SELinux AVC denials.
### I know this because as soon as I set SELinux to permissive
### (`setenforce 0`), KernelSU works completely fine with no
### apparent issues.
### I don't know how to allow KernelSU to pass AVC checks, if
### anyone knows please create an issue

* Superuser list not working & resetting on every restart

* Modules won't install & fail with 'os error 22'

  - See 'TO-DO-3-2024-06-02-01-20-23.log' in 'logs/'

  - This is something to do with mounting the image

  - No matter what version of KernelSU manager I use, the issue persists
    ~~so I am assuming it is a kernel-level issue~~ (read top)

### Improvements

* Add AnyKernel3 (somehow) since current way of installing is complicated
