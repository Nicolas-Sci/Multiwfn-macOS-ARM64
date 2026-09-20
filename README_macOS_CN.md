# Multiwfn for macOS (ARM64 / Apple Silicon) 编译版

这是专为苹果 M 系列芯片 (M1/M2/M3/M4) 原生编译的 Multiwfn 2026.9.13 (noGUI) 优化版。本版本基于 gfortran 编译，链接了 OpenBLAS 核心数学库以实现最高效的并行计算。

## 🛠 编译环境参考 (Compilation Environment)
如果您希望自行编译，以下是本可执行文件的构建环境，供参考：
- **系统架构**: macOS 26.6.2 (ARM64 / Apple Silicon)
- **编译器**: GNU Fortran (Homebrew GCC 16.2.0)
- **构建工具**: CMake 4.4.3
- **依赖库**: OpenBLAS, Flint 3.6.0, GMP 6.3.0

## ⚠️ 版权与引用声明 (IMPORTANT)
**版权声明**：本项目仅提供为 macOS 优化的编译版本。Multiwfn 软件的全部版权、原代码及相关知识产权均属于原作者 **Tian Lu (卢天)**（北京科音自然科学研究中心，Beijing Kein Research Center for Natural Sciences）。官方网站：http://sobereva.com/multiwfn

**引用要求**：如果您在发表的学术论文、学位论文或其他任何公开报告中使用了本程序，**必须**引用 Multiwfn 的官方文献：
- Tian Lu, Feiwu Chen, *J. Comput. Chem.*, **33**, 580 (2012) DOI: 10.1002/jcc.22885
- Tian Lu, *J. Chem. Phys.*, **161**, 082503 (2024) DOI: 10.1063/5.0216272

## 1. 依赖安装 (必做)

为了让程序能够在您的 Mac 上正常运行，您需要使用 [Homebrew](https://brew.sh/) 安装必备的运行库。

请打开终端，输入以下命令：
```bash
brew install gcc openblas flint
```
*(说明：`gcc` 提供 Fortran 及 OpenMP 并行运行库，`openblas` 提供高效线性代数计算，`flint` 提供分数阶导数支持。)*

## 2. 配置环境变量

1. 将解压后的文件夹（`Multiwfn_2026.9.13_macOS_ARM64_noGUI`）放在您平时存放软件的地方，例如 `~/Software/` 目录下。
2. 打开您的终端配置文件（如果是默认的 zsh，则是 `~/.zshrc`）。
3. 在文件最末尾添加以下几行代码（**请将路径替换为您实际存放该文件夹的绝对路径**）：

```bash
# Multiwfn configuration
export Multiwfnpath=/Users/您的用户名/您的路径/Multiwfn_2026.9.13_macOS_ARM64_noGUI
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
