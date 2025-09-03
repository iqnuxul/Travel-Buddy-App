# 旅游搭子App完整开发计划

## 🎯 项目概述
基于React Native + Expo + Firebase的旅游伙伴匹配应用，采用类似交友软件的推荐逻辑，根据旅游偏好、地点和MBTI匹配用户。

## 📋 完整行动清单

### 阶段1：前期准备 (预计1天)
- [ ] **环境搭建**
  - [ ] 注册GitHub账号，创建repo: `travel-buddy-app`
  - [ ] 注册Firebase账号，创建项目
  - [ ] 注册Expo账号
  - [ ] 安装开发环境 (Node.js, Expo CLI, Firebase CLI)
  - [ ] 初始化React Native Expo项目
  - [ ] 安装核心依赖包
  - [ ] 配置Firebase配置文件
  - [ ] 设置Git版本控制

- [ ] **项目结构规划**
  - [ ] 创建文件夹结构
  - [ ] 定义核心数据类型 (TypeScript interfaces)
  - [ ] 设置假数据文件 (mockData.ts)
  - [ ] 配置导航结构
  - [ ] 设置全局样式和主题

### 阶段2：核心页面实现 (预计5-7天)

#### 2.1 基础导航和布局 (1天)
- [ ] **导航系统**
  - [ ] 配置React Navigation
  - [ ] 创建Stack Navigator
  - [ ] 创建Bottom Tab Navigator
  - [ ] 设置页面路由

- [ ] **全局组件**
  - [ ] 通用头部组件 (Header)
  - [ ] 加载组件 (Loading)
  - [ ] 按钮组件 (CustomButton)
  - [ ] 输入框组件 (CustomInput)

#### 2.2 首页实现 (2天)
- [ ] **地球仪视图页面** `screens/HomeScreen.tsx`
  - [ ] 顶部用户头像 + DiceBear API集成
  - [ ] 搜索栏组件
  - [ ] 地图容器 (先用静态图片占位)
  - [ ] 底部导航按钮组 (聊天、快速添加、添加计划)
  - [ ] 图钉筛选器 (5种颜色状态)
  - [ ] 图钉点击事件处理

- [ ] **地图功能优化**
  - [ ] 集成真实地图库 (react-native-maps)
  - [ ] 图钉标记系统
  - [ ] 地图交互 (缩放、拖拽)
  - [ ] 搜索城市功能

#### 2.3 行程管理 (2天)
- [ ] **我的行程列表** `screens/TripListScreen.tsx`
  - [ ] 行程卡片组件 `components/TripCard.tsx`
  - [ ] 按日期排序逻辑
  - [ ] 添加行程按钮 (虚线样式)
  - [ ] 切换到地球仪视图按钮
  - [ ] 卡片点击进入详情

- [ ] **添加计划页面** `screens/AddPlanScreen.tsx`
  - [ ] 目的地选择 (支持"不确定")
  - [ ] 出发地选择
  - [ ] 日期选择器 (支持"随意")
  - [ ] 预算区间滑块
  - [ ] 优先级排序 (衣食住行)
  - [ ] 旅行风格多选
  - [ ] 表单验证和提交

- [ ] **计划详情页面** `screens/PlanDetailScreen.tsx`
  - [ ] 详情展示布局
  - [ ] 编辑按钮功能
  - [ ] 分享功能
  - [ ] "去找搭子"按钮

#### 2.4 用户资料系统 (1天)
- [ ] **个人资料页面** `screens/ProfileScreen.tsx`
  - [ ] 头像显示和编辑
  - [ ] 评分和认证状态
  - [ ] 自我介绍编辑
  - [ ] 基本信息 (年龄、性别、MBTI)
  - [ ] 兴趣标签选择器
  - [ ] 技能标签管理
  - [ ] 个性标签展示
  - [ ] 勋章展示区域
  - [ ] 社交媒体链接

### 阶段3：匹配和社交功能 (预计4-5天)

#### 3.1 匹配系统 (2天)
- [ ] **找搭子卡片集** `screens/MatchingScreen.tsx`
  - [ ] 卡片堆叠UI组件
  - [ ] 左右滑动手势
  - [ ] 匹配/跳过按钮
  - [ ] 卡片详情弹窗
  - [ ] 筛选浮动按钮
  - [ ] 筛选面板 (性别、预算、MBTI等)

- [ ] **匹配算法**
  - [ ] MBTI兼容性计算
  - [ ] 旅行偏好相似度
  - [ ] 地点和时间匹配
  - [ ] 推荐排序算法

#### 3.2 聊天系统 (2-3天)
- [ ] **聊天列表** `screens/ChatListScreen.tsx`
  - [ ] 对话卡片组件
  - [ ] 搜索功能
  - [ ] 状态显示 (已匹配/已成队/出行中/已评价)
  - [ ] 操作按钮 (评价、举报、删除)

- [ ] **对话框** `screens/ChatScreen.tsx`
  - [ ] 消息列表展示
  - [ ] 消息输入框
  - [ ] 发送消息功能
  - [ ] 成队申请按钮
  - [ ] 推荐话题快捷按钮
  - [ ] 实时消息同步

#### 3.3 快速功能 (1天)
- [ ] **快速添加** `screens/QuickAddScreen.tsx`
  - [ ] 语音输入组件
  - [ ] 快速匹配逻辑
  - [ ] 结果展示

- [ ] **评价系统** `screens/RatingScreen.tsx`
  - [ ] 星级评分组件
  - [ ] 勋章选择界面
  - [ ] 评价提交

### 阶段4：后端集成 (预计3-4天)

#### 4.1 Firebase集成 (2天)
- [ ] **用户认证**
  - [ ] Firebase Auth配置
  - [ ] 登录/注册页面
  - [ ] 用户状态管理

- [ ] **数据库设计**
  - [ ] Firestore集合结构设计
  - [ ] 用户资料存储
  - [ ] 行程数据存储
  - [ ] 匹配关系存储
  - [ ] 聊天消息存储

#### 4.2 实时功能 (2天)
- [ ] **实时聊天**
  - [ ] Firestore实时监听
  - [ ] 消息发送和接收
  - [ ] 未读消息计数

- [ ] **推送通知**
  - [ ] Expo Notifications配置
  - [ ] 匹配通知
  - [ ] 消息通知

### 阶段5：优化和完善 (预计2-3天)

#### 5.1 UI/UX优化 (1天)
- [ ] **视觉优化**
  - [ ] Google Fonts集成 (Noto Sans SC)
  - [ ] Material Icons集成
  - [ ] 动画效果添加
  - [ ] 响应式布局优化

#### 5.2 功能完善 (1-2天)
- [ ] **第三方集成**
  - [ ] DiceBear头像API
  - [ ] 地图API (Google Maps/高德)
  - [ ] 社交媒体API集成

- [ ] **性能优化**
  - [ ] 图片懒加载
  - [ ] 数据缓存策略
  - [ ] 内存优化

## 📊 技术栈清单

### 前端框架
- React Native (Expo)
- TypeScript
- React Navigation 6

### UI组件库
- React Native Paper
- Expo Vector Icons
- React Native Elements (可选)

### 后端服务
- Firebase Authentication
- Firestore Database
- Firebase Storage
- Firebase Cloud Functions

### 开发工具
- Expo CLI
- Firebase CLI
- Git & GitHub

### 第三方API
- DiceBear (头像生成)
- Google Maps API
- 高德地图API (国内备选)

## 🎨 设计规范

### 色彩系统
```
主色调: #4F46E5 (紫色)
辅助色: #06B6D4 (青色)
成功色: #10B981 (绿色)
警告色: #F59E0B (橙色)
错误色: #EF4444 (红色)
```

### 图钉颜色规则
- 🔴 红色: 未来1个月内
- 🟠 橙色: 3个月内
- 🟡 黄色: 6个月内
- 🟢 绿色: 无限期
- ⚫ 黑色: 已经去过

### 字体规范
- 主字体: Noto Sans SC Light 300
- 标题: Noto Sans SC Medium 500
- 强调: Noto Sans SC Bold 700

## 📁 项目文件结构

```
TravelBuddyApp/
├── src/
│   ├── components/          # 通用组件
│   │   ├── TripCard.tsx
│   │   ├── UserCard.tsx
│   │   ├── CustomButton.tsx
│   │   └── ...
│   ├── screens/            # 页面组件
│   │   ├── HomeScreen.tsx
│   │   ├── TripListScreen.tsx
│   │   ├── ProfileScreen.tsx
│   │   ├── ChatListScreen.tsx
│   │   └── ...
│   ├── navigation/         # 导航配置
│   │   └── AppNavigator.tsx
│   ├── services/          # 业务逻辑
│   │   ├── firebase.ts
│   │   ├── matchingService.ts
│   │   └── ...
│   ├── types/             # TypeScript类型定义
│   │   └── index.ts
│   ├── utils/             # 工具函数
│   │   └── helpers.ts
│   ├── constants/         # 常量配置
│   │   └── theme.ts
│   └── mockData/          # 假数据
│       └── index.ts
├── assets/                # 静态资源
├── firebase.json          # Firebase配置
└── app.json              # Expo配置
```

## 📝 关键数据结构

```typescript
interface UserProfile {
  id: string;
  avatar: string;
  name: string;
  age: number;
  gender: 'male' | 'female' | 'other';
  mbti: string;
  bio: string;
  interests: string[];
  skills: string[];
  badges: string[];
  rating: number;
  verified: boolean;
  socialLinks: {
    xiaohongshu?: string;
    spotify?: string;
  };
}

interface TravelPlan {
  id: string;
  userId: string;
  title: string;
  destination: string;
  startDate: Date;
  endDate: Date;
  budget: 'luxury' | 'normal' | 'budget';
  travelStyle: string[];
  priorities: string[];
  expectations: string;
  status: 'planned' | 'matched' | 'traveling' | 'completed';
  coordinates: { lat: number; lng: number };
}

interface Match {
  id: string;
  user1Id: string;
  user2Id: string;
  planId: string;
  status: 'pending' | 'matched' | 'teamed' | 'completed';
  chatId?: string;
  createdAt: Date;
}
```

## 🎯 今日任务重点

基于这个完整计划，今天我们专注于：

1. **环境搭建和项目初始化**
2. **基础导航结构**
3. **首页核心布局**
4. **行程列表页面**

准备好开始了吗？我们先从环境搭建开始！