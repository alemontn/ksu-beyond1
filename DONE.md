### Issues


* (RESOLVED in version 0.9.5-4.14-2)

  The kernel will be compiled with the '-dirty' suffix, since running the KernelSU
  script makes the Git repo 'detached', meaning there are uncommited/unstashed changes.
  This can cause Play Integrity to fail since it will check the kernel's name.
  Play Integrity Fix should fix this, though.
