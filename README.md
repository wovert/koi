# 锦鲤卡

## 项目介绍

### 1. 项目开发准备

- 项目描述
- 技术选型
- API 接口

### 2. 开启项目开发

- 脚手架创建项目
- 安装所有依赖/指定依赖
- 开发环境运行
- 生产环境打包与发布

### 3. 搭建项目整体界面结构

- stylus
  - 结构化，变量，函数/mixin(混合)
- vue-router
  - `router-view/router-link/keep-alive`
  - `$router`: 路由器对象，包含一些操作路由的功能函数，来实现编程式导航（跳转路由）
  - `$route`：当前路由对象，一些当前路由信息数据的容器，`path/meta/query/params`
- 项目路由拆分
- 底部导航组件：`FooterGuide`
- 导航路由组件：`Site/Search/Order/Profile`

### 4. 抽取组件

- 头部组件：`HeaderTop` 通过`slot`来实现组件通信标签结构
- 商家列表组件：`ShopList`

### 5. 登录路由组件
- 静态组件
- `FooterGuide` 的现实/隐藏；通过路由的`meta`

### 6. 后台仙姑

- 启动后台项目，理解前后台分离
- 测试后台接口：使用postman
- 修正接口文档

### 7. 前后台交互

- ajax 请求库：axios
- ajax 请求函数封装：axios+promise
- 接口请求函数封装：每个后台接口

## 项目描述

1. 锦鲤卡 WebApp + 微信公众号 + 小程序
2. 包括 商家，商品，购物车，用户等多个子模块
3. 使用 React 全家桶 + ES6 + Webpack 等前段最新最热的技术
4. 采用模块化、组件化、工程化的模式开发

## 技术选型

- 前台数据处理/交互/组件化
  - vue
  - vue-router
  - vuex 应用状态管理
  - mint-ui 组件库构建界面
  - vue-lazyload 图片懒加载
  - 滑动库
    - vue-scroller
    - better-scroll
    - swiper
  - 日期处理：
    - moment
    - date-fns
- 前后台交互
  - mock数据：mockjs 模拟后台数据接口
  - 接口测试：postman
  - ajax请求
    - vue-resource
    - axios
- 模块化
  - ES6
  - babel
- 项目构建/工程化
  - webpack
  - vue-cli
  - eslint
- CSS预编译器
  - stylus

### 前段路由

- 一级路由
  - 首页
    - /site
    - Site.vue
  - 搜索
    - /search
    - Search.vue
  - 订单
    - /order
    - Order.vue
  - 个人
    - /profile
    - Profile.vue
  - 登录
    - /login
    - Login.vue
  - 商家
    - /seller
    - Seller.vue
- 二级路由（商家的）
  - 商家商品
    - /goods
    - Goods.vue
  - 商家评价
    - /ratings
    - /Ratings.vue
  - 商家信息
    - /info
    - Info.vue

- 首页/搜索/订单/个人：显示底部导航
- 登录/商家：不显示底部导航

### API 接口

- 全程：前后台交互API接口
- 重要概念
  - API(接口)
  - 接口文档
  - 对接口
  - 联调
  - 前后台分离
  - mock数据

### 项目 vue 组件

- 重要概念
  - 模块与组件
  - 模块化/组件化/工程化
- vue组件
  - 路由组件：src/pages 下
  - 一般组件：src/components 下
  - APP
    - FooterGuide
    - 路由
      - site
        - HeaderTop
        - SellerList
        - Stars
      - Search
        - HeaderTop
      - Order
        - HeaderTop
      - Profile
        - HeaderTop
      - Login
        - AlerTip
      - Seller
        - SellerHeader
          - Stars
        - 路由
          - SellerGoods
            - CartControl
            - Food
              - RatingSelect
          - SellerRatings
            - RatingSelect
            - Split
            - Stars
          - Seller
            - Split
            - Stars

### 样式/布局/效果

- stylus 编写模块化CSS
- 图标字体
- 移动端1px 边框问题
- 移动端经典的 css sticky footer 布局
- flex 弹性布局

### 数据库设计

使用 MySQL Workbench 软件设计数据库

