# Multiwfn for macOS (ARM64 / Apple Silicon)

This is a natively compiled, optimized `noGUI` version of Multiwfn 2026.8.31 for macOS running on Apple Silicon (M1/M2/M3/M4 chips). It uses OpenBLAS for high-performance matrix operations and supports multi-threading (OpenMP).

## 1. System Requirements

Since this executable is dynamically linked, you **must** install the required dependencies using [Homebrew](https://brew.sh/).

Open your terminal and run:

```bash
brew install gcc openblas flint
```

*(Note: `gcc` provides the necessary Fortran and OpenMP runtime libraries, `openblas` is for math routines, and `flint` is for fractional derivatives support).*

## 2. Installation & Configuration

1. Place this entire folder (`Multiwfn_2026.8.31_macOS_ARM64_noGUI`) anywhere on your Mac, for example in `~/Software/Multiwfn`.
2. Open your shell configuration file (usually `~/.zshrc` or `~/.bash_profile`).
3. Add the following lines at the end of the file (be sure to replace the path with your actual folder path):

```bash
# Multiwfn configuration
export Multiwfnpath=/path/to/your/Multiwfn_2026.8.31_macOS_ARM64_noGUI
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

这是专为苹果 M 系列芯片 (M1/M2/M3/M4) 原生编译的 Multiwfn 2026.8.31 (noGUI) 优化版。本版本基于 gfortran 编译，链接了 OpenBLAS 核心数学库以实现最高效的并行计算。

## 1. 依赖安装 (必做)

为了让程序能够在您的 Mac 上正常运行，您需要使用 [Homebrew](https://brew.sh/) 安装必备的运行库。

请打开终端，输入以下命令：

```bash
brew install gcc openblas flint
```

*(说明：`gcc` 提供 Fortran 及 OpenMP 并行运行库，`openblas` 提供高效线性代数计算，`flint` 提供分数阶导数支持。)*

## 2. 配置环境变量

1. 将解压后的文件夹（`Multiwfn_2026.8.31_macOS_ARM64_noGUI`）放在您平时存放软件的地方，例如 `~/Software/` 目录下。
2. 打开您的终端配置文件（如果是默认的 zsh，则是 `~/.zshrc`）。
3. 在文件最末尾添加以下几行代码（**请将路径替换为您实际存放该文件夹的绝对路径**）：

```bash
# Multiwfn configuration
export Multiwfnpath=/Users/您的用户名/您的路径/Multiwfn_2026.8.31_macOS_ARM64_noGUI
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
