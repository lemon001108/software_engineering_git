# 🌊 智慧海洋牧场可视化系统

## 📖 项目简介

本项目为**南开大学软件工程课程大作业项目**，旨在开发一套**智慧海洋牧场可视化管理系统**，基于现代 Web 技术与数据可视化手段，实现海洋牧场设备管理、数据采集与分析、异常报警、智能问答及图片识别等多功能模块，提升海洋牧场养殖管理的智能化水平。

------

## 📬 项目组信息

- 组长：王婷睿（2210578）
- 成员：涂佳欢语（2213235）、胡可玉（2212913）、安楠（2210722）、唐苇苇（2212138）

## 📌 项目实现目标

- **数据采集与管理**：实现用户、设备、环境与养殖数据管理。
- **数据处理与可视化**：对数据进行处理分析，并以图表方式直观展示。
- **异常报警与通知**：实现数据异常阈值监控及报警通知。
- **智能化功能**：
  - 图片识别
  - 鱼类体长预测
  - 智能问答
  - 鱼类运动轨迹追踪
  - 养殖建议生成
- **支持多角色权限管理**：管理员、养殖人员、访客分级权限。

------

## 📊 系统功能模块

| 模块                 | 功能描述                                                   |
| -------------------- | ---------------------------------------------------------- |
| 用户与权限管理       | 多角色登录与权限分级，保障系统安全。                       |
| 数据上传、导出与管理 | 支持数据导入、导出，养殖日志、监测数据批量处理。           |
| 数据分析与可视化展示 | 将环境监测、养殖数据以图表、仪表盘形式展示，支持图表下载。 |
| 异常报警模块         | 实时检测异常数据，触发报警并通知相关人员。                 |
| 图片识别与体长预测   | 支持上传鱼类图片，识别种类并预测体长。                     |
| 智能问答模块         | 实现简单的智能交互问答，辅助用户了解养殖信息。             |
| 移动端适配           | 部分界面适配手机端浏览器，便于随时查看。                   |

------

## ⚙️ 项目环境与技术栈

- **后端**：Python 3.x + Flask + SQLAlchemy + PyMySQL
- **前端**：HTML + CSS + JS + Bootstrap + ECharts
- **数据库**：MySQL
- **图片识别与智能问答**：基于 Python 图像识别库、基于prompt的LLM工程

------

## 📑 安装与部署说明

### 1️⃣ 安装依赖

```bash
pip install -r requirements.txt
```

### 2️⃣ 导入数据库

将 `user.sql` 脚本导入您的 MySQL 数据库：

```sql
source user.sql;
```

### 3️⃣ 配置数据库连接

编辑 `app.py` 第 25 行，替换为您本地 MySQL 用户名、密码及数据库名称：

```python
app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql+pymysql://用户名:密码@localhost/数据库名'
```

### 4️⃣ 启动项目

```bash
python app.py
```

浏览器访问：

```
http://localhost:5000
```

------

## 👥 用户类型与权限

| 用户名    | 密码        | 权限描述                                                 |
| --------- | ----------- | -------------------------------------------------------- |
| `admin`   | `123456789` | 高级权限：管理所有页面及设备，数据导入导出，异常阈值设置 |
| `fishman` | `123654`    | 中级权限：设备控制与数据查看，但无管理员权限             |
| `visitor` | `1456`      | 基础权限：仅可浏览部分界面与图表，不可控制设备或导入数据 |

------

## 📄 项目文件结构

```
├── app.py               # 主程序入口
├── user.sql             # 数据库建表及数据脚本
├── requirements.txt     # Python依赖库清单
├── templates/           # 前端HTML页面模板
├── static/              # 静态资源（CSS、JS、图片）
├── utils/               # 图片识别与体长预测工具
└── README.md            # 项目说明文档
```

------

## 📹 项目演示视频

演示视频请见项目仓库：[GitHub链接](https://chatgpt.com/c/685cd29a-8bd4-8003-b1ee-85d270eefea5)