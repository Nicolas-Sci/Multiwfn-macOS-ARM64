# Multiwfn for macOS (ARM64 / Apple Silicon)

This repository provides an optimized, native compiled executable of **Multiwfn** (noGUI version) for macOS running on Apple Silicon (M1/M2/M3/M4/M5/M6及后续芯片). 

## ⚠️ Copyright and Citation (版权与引用声明)

**1. Copyright (版权):**
This is an unofficial compilation project to help macOS users. All source codes, copyrights, and intellectual property of the Multiwfn software strictly belong to the original author, **Tian Lu** (Beijing Kein Research Center for Natural Sciences). 
本项目仅为帮助 macOS 用户的非官方编译版本。Multiwfn 软件的全部源码、版权及知识产权均严格属于原作者 **卢天老师**（北京科音自然科学研究中心）。
* Official Website (官网): http://sobereva.com/multiwfn

**2. Citation Requirement (必须引用的文献):**
If you use this compiled program in your research, you **MUST** cite the official Multiwfn literature in your publications:
如果您在科研论文中使用了本程序，**必须**在文章中引用以下官方文献：
> - Tian Lu, Feiwu Chen, *J. Comput. Chem.*, **33**, 580 (2012) DOI: 10.1002/jcc.22885
> - Tian Lu, *J. Chem. Phys.*, **161**, 082503 (2024) DOI: 10.1063/5.0216272
 
This is a natively compiled, optimized `noGUI` version of Multiwfn [VERSION] for macOS running on Apple Silicon (M1 to M6 chips and newer). It uses OpenBLAS for high-performance matrix operations and supports multi-threading (OpenMP).

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

Enjoy!


# Multiwfn for macOS (ARM64 / Apple Silicon) 编译版

这是专为苹果 M 系列芯片 (M1/M2/M3/M4/M5/M6及后续芯片) 原生编译的 Multiwfn [VERSION] (noGUI) 优化版。本版本基于 gfortran 编译，链接了 OpenBLAS 核心数学库以实现最高效的并行计算。

## 1. 零依赖环境（便携版）

这是一个完全便携的“绿色版”。所有的核心依赖库（包括 OpenBLAS、GCC 多线程运行库、Flint 等）都已自动打包在 `lib/` 文件夹内。**您不需要安装 Homebrew、gcc 或任何其他依赖！** 下载解压即可直接运行。

## 2. 配置环境变量

1. 将解压后的文件夹（and rename it to `Multiwfn_macOS`）放在您平时存放软件的地方，例如 `~/Software/` 目录下。
2. 打开您的终端配置文件（如果是默认的 zsh，则是 `~/.zshrc`）。
3. 在文件最末尾添加以下几行代码（**请将路径替换为您实际存放该文件夹的绝对路径**）：

```bash
# Multiwfn configuration
export Multiwfnpath=/Users/您的用户名/您的路径/Multiwfn_macOS
export PATH=$PATH:$Multiwfnpath
export OMP_STACKSIZE=200M
```

4. 保存文件，关闭终端再重新打开（或者执行 `source ~/.zshrc`）。

## 3. 运行方法

现在，您可以在任意目录下直接输入：

```bash
Multiwfn
```

即可直接调用本程序啦！

祝科研顺利！
