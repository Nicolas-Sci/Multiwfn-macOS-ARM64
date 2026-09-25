# Multiwfn for macOS (ARM64 / Apple Silicon)

This is a natively compiled, optimized `noGUI` version of Multiwfn [VERSION] for macOS running on Apple Silicon (M1 to M6 chips and newer). It uses OpenBLAS for high-performance matrix operations and supports multi-threading (OpenMP).

## 🛠 Compilation Environment
If you wish to compile it yourself, here is the environment used for this build:
- **Architecture**: macOS 26.6.2 (ARM64 / Apple Silicon)
- **Compiler**: GNU Fortran (Homebrew GCC 16.2.0)
- **Build Tool**: CMake 4.4.3
- **Dependencies**: OpenBLAS, Flint 3.6.0, GMP 6.3.0

## ⚠️ Copyright & Citation Requirements
**Copyright**: This repository only provides an optimized build for macOS. All copyrights, source codes, and intellectual property of the Multiwfn software belong strictly to the original author, **Tian Lu** (Beijing Kein Research Center for Natural Sciences). Official Website: http://sobereva.com/multiwfn

**Citation**: If you use this software in your research and publish any papers, you **MUST** cite the official Multiwfn literature as follows:
- Tian Lu, Feiwu Chen, *J. Comput. Chem.*, **33**, 580 (2012) DOI: 10.1002/jcc.22885
- Tian Lu, *J. Chem. Phys.*, **161**, 082503 (2024) DOI: 10.1063/5.0216272

## 1. Zero Dependencies (Portable)

This release is fully portable. All required dynamic libraries (OpenBLAS, GCC OpenMP, Flint, etc.) are **bundled inside the `lib/` directory**. You do **NOT** need to install Homebrew, GCC, or any other dependencies. Just download and run!

## 2. Installation & Configuration

1. Place this entire folder (and rename it to `Multiwfn_macOS`) anywhere on your Mac, for example in `~/Software/Multiwfn`.
2. Open your shell configuration file (usually `~/.zshrc` or `~/.bash_profile`).
3. Add the following lines at the end of the file (be sure to replace the path with your actual folder path):

```bash
# Multiwfn configuration
export Multiwfnpath=/path/to/your/Multiwfn_macOS
export PATH=$PATH:$Multiwfnpath
export OMP_STACKSIZE=200M
```

4. Save the file and restart your terminal (or run `source ~/.zshrc`).

## 3. Running Multiwfn

Now, you can launch Multiwfn from any directory simply by typing:
```bash
Multiwfn
```
