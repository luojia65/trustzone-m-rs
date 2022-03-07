# trustzone-m-rs

ARM TrustZone-M example application in Rust, both secure world side and non-secure world side;
projects are modified from generated result of cortex-m-quickstart.

This project is based on guide _Writing secure applications using Rust and TrustZone-M, Version 1.0_
by ARM, (c) 2022 Arm Limited.

## Run

You need to install rustc target, using:

```shell
rustup target add thumbv8m.main-none-eabi
```

Use command:

```shell
cargo qemu
```

You'll get the following results:

```shell
    Finished dev [unoptimized + debuginfo] target(s) in 0.05s
     Running `target\debug\xtask.exe qemu`
xtask: make application and run in QEMU
    Finished dev [unoptimized + debuginfo] target(s) in 0.04s
    Finished dev [unoptimized + debuginfo] target(s) in 0.04s                                                                                                                                                                          
Invalid read at addr 0x10000000, size 4, region '(null)', reason: rejected
Invalid read at addr 0x10000004, size 4, region '(null)', reason: rejected
Hello from Secure World!
BLXNS with misaligned SP is UNPREDICTABLE
Hello from Non Secure World!
```

Use 'CTRL+A, X' to exit program.

