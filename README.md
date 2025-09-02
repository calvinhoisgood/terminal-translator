# 终端翻译器

一个简洁的终端翻译工具，自动将英文内容翻译为中文，提升终端使用体验。

## 🚀 快速开始

### 1. 安装依赖
```bash
pip install -r requirements.txt
```

### 2. 设置全局命令（推荐）
```bash
# 运行安装脚本
.\install_global.bat
```

### 3. 全局使用
```bash
# 使用短命令
tran -r "dir"
tran -r "python --help" 
tran -r "git status"

# 使用完整命令名
translator -r "echo Hello World"
```

### 4. 本地使用（不安装全局命令）
```bash
# 翻译命令输出
python src\translator.py --realtime "dir"
python src\translator.py --realtime "python --help" 
python src\translator.py --realtime "git status"
```

### 5. 效果展示
```
File not found
找不到文件

Permission denied
权限被拒绝
```

## ⚙️ 配置管理

### 查看当前配置
```bash
python quick_config.py show
```

### 切换翻译语言
```bash
python quick_config.py lang ja      # 日语
python quick_config.py lang zh-TW   # 繁体中文
python quick_config.py lang en      # 英语
python quick_config.py lang ko      # 韩语
python quick_config.py lang fr      # 法语
python quick_config.py lang de      # 德语
```

### 修改显示颜色
```bash
python quick_config.py color original yellow      # 原文颜色
python quick_config.py color translation green    # 译文颜色
```

## 📋 功能特点

- **主动翻译**: 自动识别英文内容并翻译
- **换行显示**: 原文和译文分行显示，清晰易读
- **Google翻译**: 免费可靠，无需API密钥
- **智能过滤**: 自动跳过路径、数字等不需要翻译的内容
- **配置简单**: 一键切换语言和颜色
- **即时生效**: 修改配置立即生效，无需重启

## 💡 使用场景

- 学习新的命令行工具
- 阅读软件帮助文档
- 理解错误信息和警告
- 查看系统状态和日志

## 📁 项目结构

```
d:\userer\
├── src\
│   ├── translator.py          # 主程序
│   ├── translation_apis.py    # Google翻译API
│   ├── display_formatter.py   # 显示格式化
│   └── config_manager.py      # 配置管理
├── quick_config.py            # 配置工具
├── install_global.bat         # 全局安装脚本
└── requirements.txt           # 依赖包
```

## ❓ 常见问题

**Q: 命令执行失败？**  
A: 确保命令用引号包裹，如：`tran -r "你的命令"`

**Q: tran 命令不识别？**  
A: 请先运行 `.\\安装脚本.bat` 安装全局命令，并确保Python Scripts目录在PATH中

**Q: 某些内容没有翻译？**  
A: 工具会自动跳过路径、数字、命令名等不需要翻译的内容

**Q: 如何获取帮助？**  
A: 运行 `tran --help` 或 `python src\translator.py --help` 查看所有选项

---

**享受无障碍的终端体验！** 🎉
