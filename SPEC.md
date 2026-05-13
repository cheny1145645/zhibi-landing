# 论文代写服务官网 - 设计规格

## 1. Concept & Vision

打造一个高端学术服务机构的视觉形象——不是廉价的代写网站，而是一个**专业、权威、值得信赖**的知识服务平台。整体风格：**深邃星空 + 流光金箔**，让客户感受到"这是一家有实力的顶级团队"。页面如同一场视觉盛宴，滚动时元素如星辰般渐次点亮，暗示着每一个idea都被精心雕琢。

## 2. Design Language

### Aesthetic Direction
- **Dark Luxury**: 深黑底色 (#050510) + 流动金箔 (#FFD700, #F5C842) + 紫罗兰高光 (#8B5CF6)
- 背景：粒子星空 + 微光流沙动画，营造深邃宇宙感
- 卡片：玻璃拟态 (glassmorphism)，半透明金边框
- 字体：中文衬线（Noto Serif SC）配英文无衬线（Playfair Display）

### Color Palette
```
--bg-deep: #050510
--bg-card: rgba(255,255,255,0.03)
--gold-primary: #FFD700
--gold-light: #F5C842
--gold-dark: #B8860B
--violet-accent: #8B5CF6
--violet-glow: #A78BFA
--text-primary: #FFFFFF
--text-secondary: rgba(255,255,255,0.65)
--border-gold: rgba(255,215,0,0.3)
```

### Typography
- **Display**: "Noto Serif SC" (Google Fonts) - 中文衬线，权威感
- **English Accent**: "Playfair Display" - 优雅衬线
- **Body**: "Inter" - 现代无衬线
- Scale: Hero 72px → Section 48px → Card 24px → Body 16px

### Motion Philosophy
- **Page Load**: 粒子背景流动 + 文字逐字浮现 (typewriter effect)
- **Scroll**: 元素从下方淡入上移，stagger 100ms
- **Hover**: 卡片金边框发光扩散 + 轻微上浮
- **Pricing**: 价格数字滚动计数动画
- **Ambient**: 背景星光粒子持续漂浮

## 3. Layout & Structure

### Sections (单页垂直滚动)
1. **Hero** - 全屏，星空背景，标语 + CTA按钮 + 飘浮粒子
2. **Services** - 4列网格，服务卡片，悬停发光
3. **Pricing** - 三档定价卡片，中间档高亮（推荐）
4. **Gallery** - 软件截图画廊，懒加载 + 灯箱
5. **Process** - 时间轴，展示服务流程
6. **Testimonials** - 客户评价轮播
7. **FAQ** - 手风琴展开
8. **CTA** - 底部全宽召唤按钮
9. **Footer** - 联系方式

### Responsive Strategy
- Desktop: 4列 → 2列 → 1列
- 保持粒子效果在移动端简化

## 4. Features & Interactions

### Hero
- 全屏背景：深色渐变 + 动态粒子（canvas）
- 主标语：渐现金色文字动画
- CTA按钮：边框流光 + hover脉冲
- 滚动指示器：动态箭头

### Pricing Cards
- 三档：基础档 / 专业档(推荐) / 旗舰档
- 旗舰档标注"最高性价比"
- 价格数字：进入视口时滚动计数
- 优惠标注：旗舰档减免显示（~~原价~~ → 优惠价）
- Hover：卡片上浮 + 金色光晕扩散

### Gallery
- 软件截图网格展示
- 点击放大灯箱
- 懒加载：图片进入视口时淡入

### FAQ
- 手风琴展开/折叠
- 展开时金色下划线动画

## 5. Component Inventory

### Button
- Primary: 金色渐变背景，深色文字
- Secondary: 透明背景，金色边框，hover发光
- States: hover(scale 1.05), active(scale 0.98)

### Card (Service/Pricing)
- 深色半透明背景
- 金色细边框 (1px)
- backdrop-filter: blur(20px)
- hover: 边框发光 + translateY(-8px)

### Badge
- 推荐标签：渐变金底
- 优惠标签：渐变紫底

### Section Title
- 英文小标题（金色，字间距大）
- 中文主标题（大号，白色）
- 底部金色装饰线

## 6. Technical Approach

- **单文件 HTML**: 所有 CSS/JS 内联
- **无依赖**: 原生 HTML/CSS/JS，无框架
- **Canvas 粒子**: 纯 JS 实现星空粒子
- **Intersection Observer**: 滚动动画触发
- **Google Fonts**: CDN 加载字体
- **占位图**: 使用 picsum.photos 作为软件截图占位

## 7. Content - 服务与定价

### 服务项目
| 服务 | 说明 | 原价 | 备注 |
|------|------|------|------|
| 论文代写 | 基础版，字数不限，含查重报告 | ¥150 | |
| 软件+论文套餐 | 软件截图 + 论文，难度定价 | ¥300-450 | 根据难度浮动 |
| 软硬结合数据 | 软件 + 论文 + 完整数据 | ~¥450 | 最高档，含一切 |
| PPT制作 | 专业PPT，含设计 | ¥60 | |
| PPT修改 | 后续修改，最高 | ¥20 | |
| 售后服务 | 全程跟进，答疑解惑 | ¥60 | 旗舰档可减¥15 |

### 旗舰档优惠
- 购买最高档位（软硬结合¥450），
- 售后服务 ¥60 → ¥45（减¥15）
- PPT修改 ¥20 → ¥5（减¥15）

### 展示截图
- 5张软件界面截图（占位图，标注"软件界面"）
