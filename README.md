# ADB Joyose 管理工具

一个用于卸载、禁用和冻结 Android 设备上 Joyose 应用的命令行工具。

## 项目介绍

Joyose 是小米设备上的一个系统应用，用于优化游戏性能。本工具提供了一个简单易用的界面，帮助用户管理设备上的 Joyose 应用。

## 功能特性

- ✅ **ADB 自动检测** - 自动检查 ADB 是否已正确安装
- ✅ **设备连接验证** - 验证手机是否通过 USB 连接并启用了 USB 调试
- ✅ **智能应用查找** - 自动搜索并识别 Joyose 应用
- ✅ **多种操作选项**
  - 卸载 Joyose 应用
  - 禁用 Joyose 应用
  - 冻结 Joyose 应用
  - 一键执行全部操作
- ✅ **智能状态检测** - 实时检查应用状态，提供相应的操作建议
- ✅ **多设备支持** - 支持连接多个设备，自动显示设备列表供选择
- ✅ **友好的用户界面** - 清晰的菜单和操作指引
- ✅ **完善的错误处理** - 详细的错误信息和解决方案

## 支持的设备

- 小米手机（MIUI 系统）
- Redmi 手机
- POCO 手机
- 其他基于 Android 系统的设备（如果安装了 Joyose 应用）

## 获取方式

### 方式一：直接下载可执行文件（推荐）

1. 从 [Releases](https://github.com/yourusername/adb-joyose-manager/releases) 页面下载最新版本的 `adb_manager.exe`
2. 直接运行即可，无需安装任何依赖

### 方式二：从源代码构建

1. 克隆仓库：
   ```bash
   git clone https://github.com/yourusername/adb-joyose-manager.git
   cd adb-joyose-manager
   ```

2. 安装依赖：
   ```bash
   pip install -r requirements.txt
   ```

3. 运行脚本：
   ```bash
   python adb_manager.py
   ```

4. （可选）打包成可执行文件：
   ```bash
   pyinstaller --onefile adb_manager.py
   ```
   生成的可执行文件将位于 `dist` 目录下

## 使用方法

1. **准备工作**：
   - 将手机通过 USB 连接到电脑
   - 确保手机已启用「开发者选项」
   - 确保已启用「USB 调试」
   - 在手机上允许电脑的 USB 调试权限

2. **运行工具**：
   - 双击 `adb_manager.exe` 或运行 `python adb_manager.py`

3. **操作流程**：
   - 工具会自动检测 ADB 安装情况
   - 自动检测连接的设备
   - 自动搜索 Joyose 应用
   - 根据菜单提示选择操作

## 操作说明

### 1. 卸载 Joyose 应用

使用 `pm uninstall --user 0` 命令卸载 Joyose 应用。

**注意**：卸载系统应用可能导致部分功能异常，请谨慎操作。

### 2. 禁用 Joyose 应用

使用 `pm disable` 命令禁用 Joyose 应用，使其无法运行。

### 3. 冻结 Joyose 应用

使用 `pm disable-user` 命令冻结 Joyose 应用，限制其在当前用户下的运行。

### 4. 执行全部操作

依次执行卸载、禁用和冻结操作，确保 Joyose 应用完全被管理。

## 常见问题

### Q: 运行时提示「未检测到已连接的设备」

A: 请检查：
- 手机是否通过 USB 连接到电脑
- 是否已启用开发者选项和 USB 调试
- 是否已在手机上允许电脑的 USB 调试权限
- 电脑是否已安装正确的 ADB 驱动

### Q: 执行操作时提示「需要 root 权限」

A: 部分系统应用的管理操作需要 root 权限。如果您的设备已 root，可以尝试使用 root 权限运行本工具。

### Q: 卸载后手机出现异常

A: 可以尝试通过以下方式恢复：
- 重启手机
- 恢复出厂设置（谨慎操作，会清除所有数据）
- 重新刷入系统固件

## 许可证

本项目采用 MIT 许可证，详见 [LICENSE](LICENSE) 文件。

## 免责声明

- 本工具仅用于学习和研究目的
- 使用本工具可能导致设备功能异常，请谨慎操作
- 作者不承担因使用本工具造成的任何损失
- 请在使用前备份重要数据

## 贡献

欢迎提交 Issue 和 Pull Request 来改进本项目。

## 致谢

- 感谢 PyInstaller 团队提供的打包工具
- 感谢所有为本项目提供建议和反馈的用户

## 更新日志

### v1.0.0
- 初始版本
- 支持卸载、禁用和冻结 Joyose 应用
- 提供友好的用户界面
- 支持多设备连接
- 智能检测应用状态
