# 蒸汽朋克怪物卡牌模板设计规范

## 一、卡牌基础规格

### 1.1 尺寸与比例
- **尺寸**: 512×768像素 (2:3竖版比例)
- **分辨率**: 72 DPI (屏幕显示)
- **安全边距**: 四周各留20像素

### 1.2 视觉风格
- **主题**: 蒸汽朋克机械风格
- **色彩**: 铜色、青铜色、深褐色为主，配合怪物元素色
- **质感**: 金属质感、齿轮纹理、蒸汽效果
- **边框**: 复杂齿轮装饰边框

## 二、卡牌布局结构

```
┌─────────────────────────┐  ← 顶部装饰条
│  [稀有度星标]  卡牌名称   │  ← 标题区
├─────────────────────────┤
│                         │
│    [怪物插画区域]        │  ← 主视觉区 (占60%)
│                         │
├─────────────────────────┤
│  类型: [攻击/防御/技能]  │  ← 类型标识
├─────────────────────────┤
│  ⚙️ [齿轮费用]          │  ← 费用区
├─────────────────────────┤
│  [卡牌效果描述]          │  ← 效果文本区
│  伤害: XX               │
├─────────────────────────┤
│  [怪物名称] [编号]       │  ← 底部信息
└─────────────────────────┘
```

## 三、稀有度配色方案

| 稀有度 | 边框颜色 | 背景色调 | 光效 |
|--------|----------|----------|------|
| 普通 ⭐ | 铜色 #B87333 | 深褐 #3D2914 | 无 |
| 稀有 ⭐⭐ | 银色 #C0C0C0 | 深蓝 #1a1a2e | 微光 |
| 史诗 ⭐⭐⭐ | 金色 #FFD700 | 深紫 #2d1b4e | 流光 |
| 传说 ⭐⭐⭐⭐ | 玫瑰金 #B76E79 | 暗红 #3d1515 | 脉冲 |
| 终极 ⭐⭐⭐⭐⭐ | 彩虹渐变 | 黑金 #0a0a0a | 闪烁 |

## 四、元素类型图标

| 元素 | 图标 | 颜色 |
|------|------|------|
| 攻击 ⚔️ | 交叉剑 | 红色 #FF4444 |
| 防御 🛡️ | 盾牌 | 蓝色 #4444FF |
| 技能 ⚙️ | 齿轮 | 黄色 #FFAA00 |
| 增益 ⬆️ | 向上箭头 | 绿色 #44FF44 |
| 减益 ⬇️ | 向下箭头 | 紫色 #FF44FF |

## 五、字体规范

- **卡牌名称**: 24px 粗体 衬线字体
- **效果文本**: 16px 常规 无衬线字体
- **数值**: 20px 等宽字体
- **描述**: 14px 斜体

## 六、装饰元素

### 6.1 边框装饰
- 四角齿轮图案
- 侧边蒸汽管道纹理
- 底部机械花纹

### 6.2 背景纹理
- 金属拉丝效果
- 细微齿轮图案
- 蒸汽朦胧效果

### 6.3 特殊效果
- 稀有卡牌: 边缘发光
- 史诗卡牌: 粒子效果
- 传说/终极: 动态光效

## 七、生成提示词模板

### 基础模板
```
Steam punk trading card design, [怪物名称], [卡牌类型] card,
[稀有度描述] border with gear decorations,
[元素颜色] accent colors,
Mechanical frame with copper and bronze details,
Steam effects, metallic texture,
Card name at top, cost indicator with gear icon,
Clean layout, game asset, 2:3 aspect ratio,
Dark background, fantasy game art style
```

### 稀有度修饰
- 普通: "copper border, simple design"
- 稀有: "silver border, glowing edges"
- 史诗: "golden border, flowing light effects"
- 传说: "rose gold border, pulsing aura"
- 终极: "rainbow prismatic border, shimmering"

## 八、文件命名规范

```
[怪物类型]_[怪物编号]_[卡牌编号]_[卡牌名称].png

示例:
- normal_01_gear_spider_01_gear_bite.png
- elite_E01_heavy_mech_01_heavy_bombardment.png
- boss_B01_titan_golem_27_titan_fall.png
```

## 九、输出目录结构

```
/workspace/cards/
├── normal/          # 普通怪物卡牌
│   ├── 01_gear_spider/
│   ├── 02_steam_beetle/
│   └── ...
├── elite/           # 精英怪物卡牌
│   ├── E01_heavy_mech/
│   ├── E02_chainsaw_berserker/
│   └── ...
└── boss/            # Boss卡牌
    ├── B01_titan_golem/
    ├── B02_chrono_dragon/
    └── ...
```
