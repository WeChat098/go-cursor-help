# Cursor Free Trial Reset Tool

[English](#english) | [中文](#chinese)

<a name="english"></a>
## English

### Description
A tool to resolve the following prompt issue during Cursor's free trial period:
```
Too many free trial accounts used on this machine. Please upgrade to pro. We have this limit in place to prevent abuse. Please let us know if you believe this is a mistake.
```

### Features
- Reset Cursor free trial limitations
- Provides both automatic and manual reset methods
- Support multiple platforms

### System Support
- ✅ Windows (Tested)
- ⚠️ MacOS (Untested)
- ⚠️ Linux (Untested)

### Automatic Reset
#### Prerequisites
- Requires administrator/root privileges
- Ensure Cursor is completely closed before use

#### Usage
1. Download the appropriate executable for your system:
   - Windows: `cursor_id_modifier.exe`
   - MacOS: `cursor_id_modifier_mac` or `cursor_id_modifier_mac_arm64`
   - Linux: `cursor_id_modifier_linux`
2. Run the program as administrator
3. Follow the prompts
4. Restart Cursor to apply changes

### Manual Reset
1. Close Cursor completely
2. Locate the storage.json file:
   - Windows: `%APPDATA%\Cursor\User\globalStorage\storage.json`
   - MacOS: `~/Library/Application Support/Cursor/User/globalStorage/storage.json`
   - Linux: `~/.config/Cursor/User/globalStorage/storage.json`
3. Make the file writable (if needed):
   - Windows: Right click -> Properties -> Uncheck "Read-only"
   - MacOS/Linux: `chmod 666 storage.json`
4. Edit the file and replace these fields with new random values:
   ```json
   {
     "telemetry.macMachineId": "generate-64-char-hex",
     "telemetry.machineId": "generate-64-char-hex",
     "telemetry.devDeviceId": "generate-uuid-format"
   }
   ```
   - For hex values: Use 64 characters (0-9, a-f)
   - For UUID: Use format like "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
5. Make the file read-only:
   - Windows: Right click -> Properties -> Check "Read-only"
   - MacOS/Linux: `chmod 444 storage.json`
6. Restart Cursor

### ⚠️ Cautions
1. Use this tool at your own risk
2. Backup important data before use
3. For educational and research purposes only

### Disclaimer
This tool is for educational purposes only. Users bear all risks and responsibilities associated with its use.

### Contributing
Issues and Pull Requests are welcome to help improve this project.

---

<a name="chinese"></a>
## 中文

### 问题描述
解决Cursor在免费订阅期间出现以下提示的问题:
```
Too many free trial accounts used on this machine. Please upgrade to pro. We have this limit in place to prevent abuse. Please let us know if you believe this is a mistake.
```

### 功能特性
- 重置Cursor免费试用限制
- 提供自动和手动重置方法
- 支持多个操作系统平台

### 系统支持
- ✅ Windows (已测试)
- ⚠️ MacOS (未测试)
- ⚠️ Linux (未测试)

### 自动重置
#### 使用前提
- 需要管理员/root权限执行
- 请确保已完全退出Cursor程序

#### 使用方法
1. 下载对应系统的可执行文件：
   - Windows系统：`cursor_id_modifier.exe`
   - MacOS系统：`cursor_id_modifier_mac` 或 `cursor_id_modifier_mac_arm64`
   - Linux系统：`cursor_id_modifier_linux`
2. 以管理员身份运行程序
3. 按照提示进行操作
4. 重启Cursor即可

### 手动重置
1. 完全关闭Cursor
2. 找到storage.json文件：
   - Windows: `%APPDATA%\Cursor\User\globalStorage\storage.json`
   - MacOS: `~/Library/Application Support/Cursor/User/globalStorage/storage.json`
   - Linux: `~/.config/Cursor/User/globalStorage/storage.json`
3. 修改文件为可写（如果需要）：
   - Windows: 右键 -> 属性 -> 取消勾选"只读"
   - MacOS/Linux: `chmod 666 storage.json`
4. 编辑文件，替换以下字段为新的随机值：
   ```json
   {
     "telemetry.macMachineId": "生成64位十六进制",
     "telemetry.machineId": "生成64位十六进制",
     "telemetry.devDeviceId": "生成UUID格式"
   }
   ```
   - 十六进制值：使用64个字符(0-9, a-f)
   - UUID格式：类似 "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
5. 将文件设为只读：
   - Windows: 右键 -> 属性 -> 勾选"只读"
   - MacOS/Linux: `chmod 444 storage.json`
6. 重启Cursor

### ⚠️ 注意事项
1. 使用本工具需要您自行承担风险
2. 建议在重要数据做好备份后使用
3. 本工具仅用于学习研究,请勿用于商业用途

### 免责声明
本工具仅供学习交流使用,使用本工具所造成的任何问题由使用者自行承担。

### 贡献
欢迎提交Issue和Pull Request来帮助改进这个项目。

## License
MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.






