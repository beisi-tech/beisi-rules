# 项目结构示例
├── client/ # 前端代码  
│ ├── static/ # 静态资源  
│ ├── src/ # 前端源代码  
│ │ ├── components/ # 可复用组件  
│ │ ├── pages/ # 页面组件  
│ │ ├── assets/ # 样式、图片等  
│ │ ├── services/ # API请求  
│ │ └── utils/ # 工具函数  
│ └── package.json # 前端依赖  
├── server/ # 后端代码  
│ ├── src/ # 后端源代码  
│ │ ├── controllers/ # 控制器  
│ │ ├── models/ # 数据模型  
│ │ ├── routes/ # 路由  
│ │ ├── middlewares/ # 中间件  
│ │ ├── services/ # 业务逻辑  
│ │ ├── config/ # 配置文件  
│ │ └── utils/ # 工具函数  
│ └── package.json # 后端依赖  
└── README.md # 项目说明  
  
  
## 目录说明

### 前端 (`client/`)
- **`static/`**: 存放静态资源（如图片、字体等）。
- **`src/`**: 存放前端源代码。
  - **`components/`**: 存放可复用的UI组件。
  - **`pages/`**: 存放页面组件。
  - **`assets/`**: 存放样式、图片等资源。
  - **`services/`**: 存放与后端交互的API请求代码。
  - **`utils/`**: 存放工具函数。
- **`package.json`**: 前端项目的依赖配置文件。

### 后端 (`server/`)
- **`src/`**: 存放后端源代码。
  - **`controllers/`**: 存放处理请求的控制器。
  - **`models/`**: 存放数据模型。
  - **`routes/`**: 存放路由定义。
  - **`middlewares/`**: 存放中间件。
  - **`services/`**: 存放业务逻辑。
  - **`config/`**: 存放配置文件。
  - **`utils/`**: 存放工具函数。
- **`package.json`**: 后端项目的依赖配置文件。

### 根目录
- **`README.md`**: 项目说明文档。