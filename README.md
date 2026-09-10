# MFS｜超广角畸变产品影像风格 Skill v1.0

**MFS | Extreme Ultra-Wide Distortion Product Visual Skill**

> Cinematography × AIGC × Product Visual Language

由 **漫反射studio / MFS STUDIO** 整理与发布。  
这是一个面向 AIGC 商业视觉创作的影像风格 Skill，用于快速生成具有 **极端超广角透视、近大远小、前景产品巨大化、真实动作轨迹、硬阳光 + 硬闪光** 特征的静帧与视频提示词。

---

## 原创声明

> **【skill原创作者（小红书同名）：漫反射studio，请勿商用转卖，如有发现必将追责.】**

Skill 本体中已经包含 `first_use_popup` 配置，用于在支持该字段的平台首次导入 / 首次使用时显示原创声明与使用提醒。  
不同平台对自定义 Skill JSON 的字段支持方式不同，如目标平台不支持弹窗字段，请保留本 README 中的原创声明并在发布页显著展示。

---

## 这套风格解决什么问题？

传统产品人像摄影很容易出现：

**人物很好看，但产品没有成为第一视觉中心。**

本 Skill 的方法是主动改变空间层级：

**产品前景层 ＞ 四肢动作层 ＞ 人物主体层 ＞ 建筑 / 场景背景层**

通过摄影机极度贴近产品，让产品在透视中自然巨大化，而不是简单后期放大。人物和场景的作用，是为产品建立动作、尺度、速度与空间张力。

核心理念：

> **通过“破坏正常比例”，重建商业视觉层级。**

---

## 核心视觉 DNA

### 1. 极端近距超广角

推荐使用：

- `10–14mm rectilinear ultra-wide lens`
- `extreme wide-angle perspective`
- `camera extremely close to the foreground product`
- `exaggerated near-far perspective`
- `strong edge stretching`
- `dramatic foreshortening`
- `perspective distortion`

重点不只是“广”，而是 **摄影机与前景产品的距离极近**。

---

### 2. 前景产品巨大化

产品必须成为画面的绝对第一视觉中心。

常见画面层级：

```text
巨大前景产品
↓
手 / 腿 / 动作
↓
人物主体
↓
建筑 / 城市 / 天空
```

通常让：

```text
产品视觉尺寸 > 人物头部视觉尺寸
```

---

### 3. 真实动作轨迹

产品的巨大尺度应来自 **摄影机主动进入产品正常运动轨迹附近**，而不是人物刻意把产品送到镜头前。

推荐：

- 真跑
- 真跳
- 真跨栏
- 真落地
- 真跨步
- 真扑出
- 真承重

避免：

- 为展示产品主动伸脚
- 主动把饮料递向镜头
- 机械劈叉
- 没有重心和惯性的摆拍动作

---

### 4. 硬阳光 + 硬闪

默认光影逻辑：

- 晴天硬阳光
- 明确明暗交界
- 大面积深阴影
- 锐利高光
- `side flash / direct flash`
- 高对比商业广告质感

常用组合：

```text
Sunlight + Hard Side Flash
```

---

### 5. 都市青年空间

特别适合：

- CBD 城市广场
- 网球场 / 篮球场
- 地下通道
- 工业道路
- 屋顶平台 / 停车场
- 商业街
- 游乐园
- 城市运动空间

这些场景中的建筑、围栏、墙面、道路、钢结构，可以在超广角下形成强烈放射透视。

---

## 适用产品

这套方法特别适合：

- 老爹鞋
- 跑鞋 / 运动鞋
- 饮料
- 口红 / 美妆
- 墨镜 / 眼镜
- 包袋
- 潮流配件
- 具有明显造型结构的产品

---

## 静帧提示词输出结构

当用户要求生成静帧提示词时，Skill 默认使用以下结构：

```text
1.【画面类型 / 构图】
2.【产品设定】
3.【人物设定】
4.【人物动作】
5.【超广角摄影机逻辑】
6.【产品突出逻辑】
7.【场景】
8.【背景色彩】
9.【光影】
10.【闪光灯】
11.【景深】
12.【完整合并版提示词】
13.【负面约束】
```

---

## 视频提示词输出结构

当用户要求生成视频提示词时，Skill 默认使用：

```text
1.【场景与影调全局】
2.【人物设定】
3.【运镜与画面逻辑】
4.【分镜头时间轴】
```

---

## 视频核心方法：Speed Ramp

对于运动类产品视频，Skill 默认支持：

```text
正常高速动作
↓
产品即将进入摄影机最近距离
↓
Speed Ramp
↓
慢动作 Product Hero Moment
```

典型结构：

- 前半段：正常极速动作
- 临界点：产品进入最近空间层
- 后半段：约 8× 慢动作展示产品

例如：

- 鞋底越镜
- 跨栏落地
- 冲入镜头
- 鞋子触地承重
- 中底压缩与回弹
- 悬浮产品追逐

---

## 景深逻辑

### 大景深

适合突出：

- 超广角空间
- 建筑发散
- 产品、人物、环境之间的尺度关系

### 浅景深

适合明确的 Product Hero Shot：

```text
锐利产品
↓
轻微虚化四肢
↓
虚化人物
↓
进一步虚化环境
```

用户明确要求浅景深时，Skill 默认：

> **焦点优先锁定产品。**

---

## 调用方法

### 静帧

```text
请用「MFS｜超广角畸变产品影像风格 Skill」写一条静帧提示词：

产品是【银灰老爹鞋】
人物是【年轻亚洲运动潮男】
动作是【高速跨栏】
场景是【CBD城市广场】
重点展示【鞋侧结构 + 厚底】
景深要求【浅景深】
光影要求【晴天硬阳光 + 侧闪】
```

---

### 视频

```text
请用「MFS｜超广角畸变产品影像风格 Skill」写一条视频提示词：

时长【4秒】
镜头结构【单镜头】
产品【老爹鞋】
人物动作【高速跑向镜头】
场景【地下通道】
镜头运动【镜头与人物高速对冲】
快慢变速【前2秒正常高速，后2秒8倍慢动作】
重点展示【鞋面结构 + 中底触地压缩与回弹】
```

---

## 推荐关键词

### Camera

```text
10–14mm rectilinear ultra-wide lens
extreme wide-angle perspective
fisheye feel
ground-level camera
high-angle overhead shot
lens pointing upward
camera extremely close to the foreground product
dynamic perspective distortion
oversized foreground product
```

### Product

```text
product hero shot
product-first composition
foreground product dominance
detailed outsole texture
visible upper construction
thick sole silhouette
material clarity
structural layering
```

### Motion

```text
authentic running motion
realistic jump trajectory
natural lunge
true landing impact
athletic force
body momentum
not posing for the product
camera actively approaches the product path
```

### Lighting

```text
bright hard sunlight
sharp light-shadow boundary
side flash lighting
direct flash feel
dark shadow base
high contrast commercial lighting
```

### Mood

```text
youth streetwear
urban sports editorial
rebellious cool energy
dynamic fashion campaign
high-impact commercial photography
contemporary product cinematography
```

---

## 默认约束

Skill 默认遵守：

1. 产品优先于人物。
2. 产品巨大化来自真实空间距离与动作轨迹。
3. 人物动作必须符合真实重心、惯性和发力逻辑。
4. 禁止人物主动把产品递向镜头。
5. 场景必须服务于透视与空间纵深。
6. 默认硬阳光 + 硬闪光。
7. 保留高对比、暗调阴影与商业摄影质感。
8. 浅景深时优先对焦产品。
9. 视频可默认使用前快后慢 Speed Ramp。
10. 除非用户明确要求，不添加字幕、无关特效与花哨图形。

---

## 负面约束方向

默认需要避免：

```text
普通站姿
产品过小
人物抢主视觉
弱透视
长焦压缩感
人物主动展示产品
没有真实运动惯性
产品结构错误
鞋型融化
额外肢体
机械动作
廉价复杂背景
高饱和杂色
柔和小清新光线
卡通化
插画化
```

---

## 文件说明

本发布包包含：

```text
MFS_UltraWide_Distortion_Product_Visual_Skill_v1.0/
├── README.md
└── MFS_UltraWide_Distortion_Product_Visual_Skill_v1.0.json
```

- `README.md`：GitHub / Skill 分享页说明文档
- `MFS_UltraWide_Distortion_Product_Visual_Skill_v1.0.json`：Skill 本体

---

## 关于 MFS STUDIO

**MFS STUDIO / 漫反射studio**

**Cinematography × AIGC × Visual Language**

以摄影与电影视觉语言为基础，将摄影、美术、光影、镜头语言、调度与导演思维，转译为可被生成式 AI 理解和执行的方法。

---

## License / 使用说明

本 Skill 以 **免费技术交流与学习分享** 为目的公开。

**不代表商业版权授权。禁止将本 Skill 本体、修改版或重新封装版本用于转卖、付费分发、商业二次售卖。**

如需商业授权、合作或其他使用方式，请联系原创作者 **漫反射studio / MFS STUDIO**。
