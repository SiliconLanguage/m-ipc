# m-ipc

A bare-metal, hardware-assisted messaging framework built for massively parallel RISC-V clusters.

## Overview

`m-ipc` is the standalone software data plane extracted from the [MemPool](https://github.com/SiliconLanguage/mempool) hardware simulator. It provides the inter-process communication primitives and message-passing infrastructure for 1024-core RISC-V clusters.

## Repository Structure

```
m-ipc/
├── hw/
│   └── mempool/        # MemPool hardware simulator (git submodule)
└── ...                 # Software data plane (promoted from mempool-ipc/)
```

## Getting Started

Clone the repository and initialise the hardware simulation submodule:

```bash
git clone https://github.com/SiliconLanguage/m-ipc.git
cd m-ipc
git submodule update --init --recursive
```

Refer to `hw/mempool/BUILD_GUIDE.md` for instructions on building the simulation environment.

## License

BSD-2-Clause Plus Patent License — see [LICENSE](LICENSE) for details.