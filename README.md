# m-ipc

A bare-metal, hardware-assisted messaging framework built for massively parallel RISC-V clusters.

## Overview

`m-ipc` is the standalone software data plane extracted from the [MemPool](https://github.com/SiliconLanguage/mempool) hardware simulator. It provides lock-free inter-process communication primitives and message-passing infrastructure designed for many-core RISC-V systems.

## Repository Structure

```text
m-ipc/
├── docs/                                 # Architecture, run books, and routing notes
├── dataplane-emu/                        # C++ host/offload data-plane emulation
├── phase0_c/                             # Ground-truth C implementation
├── phase1_rust/                          # no_std Rust implementation
├── hw/
│   └── mempool/                          # MemPool simulator submodule
└── ...
```

## Getting Started

```bash
git clone https://github.com/SiliconLanguage/m-ipc.git
cd m-ipc
git submodule update --init --recursive
```

Refer to `hw/mempool/BUILD_GUIDE.md` for hardware simulation build steps.

## Origin

This repository contains the extracted history of `software/mempool-ipc/` from the upstream MemPool monorepo, merged with bootstrap files prepared in `m-ipc`.

## License

BSD-2-Clause Plus Patent License.
