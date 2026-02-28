# APL-Skeleton

在接触 APL 语言并对其产生兴趣之后，如何开始编写自己的应用程序，并使其能够与 GitHub 集成、方便部署？

APL-Skeleton 是一个基础骨架项目，旨在帮助你快速上手，编写可独立运行且易于部署的 APL 应用程序。本项目采用基于 SALT 的 Git 友好方式，使用纯文本文件存储源代码，而非传统的工作区文件。

本骨架项目包含以下内容：

* 用于编写代码的命名空间脚本（Namespace Script）
* 演示如何从文件启动应用程序的 DYAPP 文件
* 演示如何使用工作区创建自动启动应用程序的 `.dws` 工作区文件
* 基于 APLUnit 的单元测试框架示例

## 快速开始

首先，加载 HelloWorld 工作区：

**Windows 系统：** 双击 `HelloWorld` 工作区文件即可打开。

**Linux 系统：** 在终端中 `cd` 进入 `APL-Skeleton` 目录，然后运行：
```
mapl HelloWorld
```

**Mac 系统：** 在 APL 会话中使用 `]cd` 切换到 `APL-Skeleton` 目录，然后运行：
```
)load ./HelloWorld.dws
```

加载工作区后，终端会输出一些有用的入门命令，你可以逐一尝试以熟悉操作。

## 使用 DYAPP 脚本

`Run.dyapp` 文件演示了如何使用 DYAPP 脚本来启动 APL 应用程序，而无需依赖工作区文件。

* **Windows 系统：** 直接双击 `Run.dyapp` 文件即可运行。
* **Linux / Mac 系统：** 在终端中运行 `dyalog Run.dyapp`。

## 修改与扩展代码

主要代码位于 `HW.dyalog` 文件中，你可以通过以下方式编辑：

* 使用任意文本编辑器直接修改 `HW.dyalog` 文件；
* 或者在 APL 会话中运行以下命令打开内置编辑器（退出编辑窗口时会提示保存文件）：
  ```
  )ed HW
  ```

修改完成后，保存工作区：
```
)save
```

## 运行单元测试

本项目使用 [APLUnit](https://github.com/Gianfrancoalongi/APLUnit) 作为单元测试框架。测试文件位于 `tests/` 目录下。

在 APL 会话中运行以下命令执行测试：
```
UT.run '.\tests'
```

如需添加新的测试，请参考 `tests/HelloWorld_tests.dyalog` 文件中的示例，遵循相同的命名规范（函数名以 `_TEST` 结尾）。

建议将 `UT.dyalog` 文件直接复制到你的项目仓库中使用。如果你在使用过程中添加了新功能，欢迎向上游仓库提交 Pull Request。

## 目录结构

```
APL-Skeleton/
├── HW.dyalog              # 主命名空间，编写你的核心代码
├── Run.dyapp              # DYAPP 启动脚本
├── HelloWorld.dws         # 预构建的工作区文件（自动启动示例）
├── UT.dyalog              # APLUnit 单元测试框架
├── tests/
│   └── HelloWorld_tests.dyalog  # 单元测试示例
└── LICENSE
```

## 学习资源

以下资源可以帮助你进一步学习 APL：

* [Dyalog APL 官方教程](http://tutorial.dyalog.com)
* [Dyalog APL 入门介绍](http://www.dyalog.com/intro)
* [Dyalog 教学视频](http://www.dyalog.tv)
* [J 语言相关论文（APL 族语言背景）](http://www.jsoftware.com/papers/)
