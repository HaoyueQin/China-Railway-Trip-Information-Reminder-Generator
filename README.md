# 中国铁路行程信息提示生成器

> China Railway Trip Information Reminder Generator (CRTIRGen)

一个纯前端的中国铁路行程信息提示图片生成工具。填入乘车信息，即可生成仿真的行程信息提示单，保存为图片使用。

## 致谢

本项目基于 [lijiaxuan1811 (yuanretro)](https://github.com/yuanretro) 的原作 **[China-Railway-Trip-Information-Reminder-Generator](https://github.com/yuanretro/China-Railway-Trip-Information-Reminder-Generator)** 进行了前端界面的重新设计与完善。

原作者实现了铁路票号编码规则解析与 Canvas 绘制的核心逻辑，特此致谢！

## 与原版的区别

| 项目 | 原版 | 本版 |
|------|------|------|
| 样式 | 无样式文件，页面结构裸露 | 完整的 Glassmorphism 浅色主题 |
| 布局 | 单列堆叠 | 双列网格（表单 + 预览） |
| 交互 | 生硬展开/折叠 | 手风琴平滑展开动画 |
| 响应式 | 不支持 | 桌面/平板/手机三档适配 |
| 可维护性 | 样式与结构耦合 | 样式独立，结构清晰 |

## 功能

- 生成仿真中国铁路行程信息提示图片
- 支持填写：车次、站点、时间、票价、座位、证件信息等
- 支持铁路磁票票号、电子票号、出单号码的编码规则说明
- 一键生成，右键保存为图片

## 使用方法

### 本地运行

直接双击 `crtirgen.html` 用浏览器打开即可使用（推荐 Chrome / Edge / Firefox）。

### 在线使用

~~访问 http://www.yuanshen.dev/crtirgen.html~~ （原在线版已不可用，建议本地运行）

## 填写说明

| 字段 | 说明 |
|------|------|
| 车站 TMIS 码 | 每个铁路车站的唯一 5 位编号，可前往 [rail.re](https://rail.re/) 查询 |
| 机器类型 | 00-09 人工售票窗口 / 20-29 车票代售点 / 30-39 自动售票机 |
| 电子票号 | 25 位数字，构成规则见页面内折叠说明 |
| 证件号码 | 敏感数字可用 `*` 代替 |

## 文件结构

```
China-Railway-Trip-Information-Reminder-Generator/
├── crtirgen.html    # 主页面（表单 + 画布）
├── crtirgen.js      # 核心绘制逻辑
├── style.css        # 界面样式（Glassmorphism 主题）
├── img1.gif         # 中国铁路 Logo
├── img2.gif         # 二维码
├── gichn_mini_zhlv1.ttf  # 中文字体文件
├── LICENSE
└── README.md
```

## 技术栈

- 原生 HTML + CSS + JavaScript
- Canvas 2D API 绘制
- Glassmorphism 设计风格（`backdrop-filter`）
- 零外部依赖，无需构建工具

## 许可

MIT License

Copyright (c) 2024 [lijiaxuan (yuanretro)](https://github.com/yuanretro) — 核心逻辑原作者
Copyright (c) 2025 HaoyueQin — 前端界面完善

## 注意事项

- 此工具生成的图片仅供个人参考使用，请遵守国家法律法规
- 本站不会收集任何个人信息
- 如有问题或建议，欢迎提交 [Issue](https://github.com/HaoyueQin/China-Railway-Trip-Information-Reminder-Generator/issues)