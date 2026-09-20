# 实验记录工具

一个轻量级的单文件实验记录工具，用于按次数记录实验的成功、失败、备注和子任务结果，并在实验结束后导出 TXT 报告。
工具完全运行在浏览器中，不需要安装依赖、启动服务器或连接数据库。

<img width="743" height="641" alt="Screenshot 2026-09-20 at 2 42 37 PM" src="https://github.com/user-attachments/assets/3d369ac9-b5e8-4652-91a0-9756512d4550" />

## 功能

- 设置实验名称和计划次数
- 逐次记录成功或失败，并实时统计成功率
- 为每次实验添加标题和备注
- 添加多个子任务，分别记录成功、失败或未记录
- 查看并删除已记录的实验结果
- 提前结束实验
- 完成后自动下载 TXT 报告，也可手动重新下载
- 使用浏览器本地存储备份未完成的实验，并在下次打开时恢复
- 适配桌面和移动端页面

## 使用方法

### 1. 获取项目

```bash
git clone https://github.com/RaeXuu/experiment-tracker.git
cd experiment-tracker
```

也可以直接从 GitHub 下载项目压缩包并解压。

### 2. 打开工具

直接用浏览器打开 `experiment-tracker.html`，无需额外安装或配置。

### 3. 记录实验

1. 输入实验名称和实验总次数。
2. 点击“开始实验”。
3. 根据需要添加子任务、标题和备注。
4. 为当前实验选择“成功”或“失败”。
5. 完成全部次数后，浏览器会自动下载实验记录报告。

## 数据与配置

项目没有配置文件或后端服务。未完成的实验记录会保存在当前浏览器的 `localStorage` 中；实验完成、提前结束或重新开始后，备份会被清除。

所有数据均在本地浏览器中处理。清除浏览器站点数据可能会删除尚未完成的实验备份。

## 技术栈

- HTML5
- CSS3
- 原生 JavaScript
- Browser Local Storage API

## 项目结构

```text
experiment-tracker/
├── experiment-tracker.html  # 页面、样式和全部功能
└── README.md                # 项目说明
```

## 开发

项目的 HTML、CSS 和 JavaScript 均位于 `experiment-tracker.html` 中。修改后刷新浏览器即可查看结果，不需要构建步骤。

建议使用现代浏览器运行，以确保本地存储和文件下载功能正常工作。

