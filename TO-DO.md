### Issues

* The kernel will be compiled with the '-dirty' suffix, since running the KernelSU
  script makes the Git repo 'detached', meaning there are uncommited/unstashed changes.
  This can cause Play Integrity to fail since it will check the kernel's name.
  Play Integrity Fix should fix this, though.

* Superuser list not working & resetting on every restart

* Modules won't install & fail with 'os error 22'

  - See '2024-06-02-01-20-23.log' in 'logs/'

  (This is something to do with mounting the image)

  (I don't know what 'os error 22' means, if anyone knows please create an issue!!)

### Improvements

* Add AnyKernel3 (somehow) since current way of installing is complicated
