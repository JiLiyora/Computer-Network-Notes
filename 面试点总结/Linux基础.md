# 常见的Linux系统
- **Debian系**
	- Debian
	- Ubuntu
	- Kali
- **Red Hat系**
	- RHEL
	- CentOS
	- Fedora
- ...

# Linux系统的管理组成
## Linux内核
## shell
## 文件系统
## 应用层程序

# 动态库和静态库的区别

|               | 静态库           | 动态库            |
| ------------- | ------------- | -------------- |
| **拓展名**       | `.a` / `.lib` | `.so` / `.dll` |
| **是否编译到目标程序** | 是             | 否              |

# make
- `make`是GNU提供的一种<font color="#ff0000">半自动化的工程管理器</font>
	- <font color="#00b0f0">半自动化</font>是指在使用工程管理器之前需要<font color="#ff0000">人工编写</font>程序的<font color="#ff0000">编译规则</font>, 所有编译规则都保存在makefile文件中
	- 全自动化的工程管理器会在编译程序前自动生成makefile文件

| 无 Make        | 有 Make               |
| ------------- | -------------------- |
| 手动输入冗长命令      | 一键构建 (`make`)        |
| 全量编译，效率低下     | **增量编译**，极大提升效率      |
| 依赖关系靠人脑记忆，易出错 | 依赖关系明确定义在 Makefile 中 |
| 构建过程不一致，易出错   | 构建过程标准化，可重复          |

# make和makefile的区别
- `make`是一个<font color="#ff0000">命令行工具</font>, 用于自动化构建和管理项目. 根据`makefile`的规则决定如何编译、链接或执行
- `makefile`是一个<font color="#ff0000">文本文件</font>, 包含了一些列规则, 告诉`make`如何构建目标

# cmake
`cmake`是一个跨平台的开源构建系统生成器, 用于管理和自动化软件项目的编译过程. 它本身不直接编译代码, 而是根据`CMkaeLists.txt`生成适用于不同平台和编译器的构建文件, 然后由对应的底层构建工具来实现执行编译

# WSL
- Windows Subsystem for Linux
- Windows系统的Linux子系统

# 编译过程中链接的优化
- 减少全局符号
	- 尽量使用`static`将函数和变量限制在文件作用域内
- 