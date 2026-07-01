---
name: web-animation
description: Add anime-style visual elements to websites — anime background images, anime avatars, and larger rounded corners. Use when the user asks to add anime style, ACG elements, 二次元风格, or anime-themed visuals to a web page or component.
---

# Web Anime Style

为网站添加动漫风格的视觉元素，让页面更具二次元氛围。

## 0. 前置检查（重要，先做这一步）

在写任何代码之前：

1. **直接使用下方"图片资源"表中给出的在线 URL**，无需本地文件、无需 `ls` 检查、无需关心项目静态资源目录结构。所有图片均为外部 CDN 链接（`http://101.96.214.171:40027/...`），可直接写入 `src` / `background-image`。
2. **确认现有项目配色**：检查项目是否已有品牌色 / Tailwind 主题色配置（`tailwind.config.js` 的 `theme.colors`）。若已有强品牌色，动漫配色（粉/紫/天蓝）应作为**点缀色**叠加，不要整体替换主色，避免视觉冲突。
3. **图床为 HTTP（非 HTTPS）**：若项目部署在 HTTPS 站点下，浏览器可能因 Mixed Content 策略拦截这些图片。若遇到图片不显示，检查浏览器控制台是否有 Mixed Content 警告，并考虑：a) 将图片下载到本地项目自行托管；b) 或通过反向代理转为 HTTPS。

## 图片资源（在线 CDN）

所有动漫图片均为在线 URL，按用途分为三类：头像、竖版背景、横版背景。直接复制下方 URL 使用。

### 头像（avatar，正方形，适合用户/作者/评论区头像）

| 用途 | URL | 尺寸 |
|------|-----|------|
| 主头像 01 | `http://101.96.214.171:40027/i/2026/06/14/6a2e7136667d7.webp` | 700×700 |
| 头像 02 | `http://101.96.214.171:40027/i/2026/06/14/6a2e713b05ae5.webp` | 250×250 |
| 头像 03 | `http://101.96.214.171:40027/i/2026/06/14/6a2e713a4032f.webp` | 250×250 |
| 头像 04 | `http://101.96.214.171:40027/i/2026/06/14/6a2e713a65793.webp` | 700×700 |
| 头像 05 | `http://101.96.214.171:40027/i/2026/06/14/6a2e71399be58.webp` | 250×250 |
| 头像 06 | `http://101.96.214.171:40027/i/2026/06/14/6a2e7139ad4f6.webp` | 250×250 |
| 头像 07 | `http://101.96.214.171:40027/i/2026/06/14/6a2e7139129d1.webp` | 250×250 |
| 头像 08 | `http://101.96.214.171:40027/i/2026/06/14/6a2e71391b7aa.webp` | 250×250 |

### 竖版背景（col，适合 Hero、卡片背景、侧边栏，配合 `object-cover`）

| 用途 | URL | 尺寸 |
|------|-----|------|
| 竖图 01 | `http://101.96.214.171:40027/i/2026/06/14/6a2e713c399c4.webp` | 1371×2122 |
| 竖图 02 | `http://101.96.214.171:40027/i/2026/06/14/6a2e713b39ecf.webp` | 761×1024 |
| 竖图 03 | `http://101.96.214.171:40027/i/2026/06/14/6a2e713ae91de.webp` | 675×900 |
| 竖图 04 | `http://101.96.214.171:40027/i/2026/06/14/6a2e713a7b7e1.webp` | 675×900 |
| 竖图 05（人物立绘） | `http://101.96.214.171:40027/i/2026/05/21/6a0dede9cd12e.jpg` | 1000×2252 |
| 竖图 06（人物立绘） | `http://101.96.214.171:40027/i/2026/06/15/6a2eef614e150.jpg` | 902×1200 |
| 竖图 07（人物立绘） | `http://101.96.214.171:40027/i/2026/06/15/6a2eef61eda2b.jpg` | 997×1004 |
| 竖图 08（人物立绘） | `http://101.96.214.171:40027/i/2026/06/15/6a2eef5d3a42f.jpg` | 756×1200 |
| 竖图 09（人物立绘） | `http://101.96.214.171:40027/i/2026/06/15/6a2eef5a7af64.jpg` | 675×1200 |
| 竖图 10（人物立绘） | `http://101.96.214.171:40027/i/2026/06/15/6a2eef5a48bf5.jpg` | 800×1200 |
| 竖图 11（人物立绘） | `http://101.96.214.171:40027/i/2026/06/15/6a2eef59b2cb7.jpg` | 554×1200 |

### 横版背景（row，适合 Banner、Hero、全宽背景）

| 用途 | URL | 尺寸 |
|------|-----|------|
| 横图 01（超大） | `http://101.96.214.171:40027/i/2026/06/14/6a2e74194f0f7.webp` | 6472×4000 |
| 横图 02（超大） | `http://101.96.214.171:40027/i/2026/06/14/6a2e741546274.webp` | 4230×2379 |
| 横图 03（4K） | `http://101.96.214.171:40027/i/2026/06/14/6a2e7415e0bd7.webp` | 3840×2160 |
| 横图 04 | `http://101.96.214.171:40027/i/2026/06/14/6a2e74142106d.webp` | 2000×1126 |
| 横图 05 | `http://101.96.214.171:40027/i/2026/06/14/6a2e7413bb6f5.webp` | 1200×816 |
| 横图 06 | `http://101.96.214.171:40027/i/2026/06/14/6a2e7412d896b.webp` | 1200×856 |
| 横图 07（宽屏） | `http://101.96.214.171:40027/i/2026/06/14/6a2e7412e8a70.webp` | 1200×675 |

> 直接引用上述完整 URL（含 `http://101.96.214.171:40027/...`）。Hero/Banner 优先选横图 01-03（超大尺寸，适合全屏不糊）；移动端或带宽敏感场景可选横图 04-07（文件更小）。

## 操作步骤

### 1. Hero 区域使用动漫背景

- 优先使用横版图片（横图 01-07）作为 Hero 区背景
- 也可以用竖版图片（竖图 01-11），配合 `object-cover` 裁剪
- 直接使用"图片资源"表中的完整 URL
- 可使用 Next.js 的 `Image` 组件或 CSS `background-image`
- 背景上加一层半透明黑色遮罩（`bg-black/40` 或 `bg-black/50`）保证文字可读性

```tsx
// 示例：Hero 背景
<section className="relative h-screen overflow-hidden">
  <img
    src="http://101.96.214.171:40027/i/2026/06/14/6a2e74194f0f7.webp"
    alt=""
    className="absolute inset-0 w-full h-full object-cover"
  />
  <div className="absolute inset-0 bg-black/40" />
  <div className="relative z-10 flex flex-col items-center justify-center h-full text-white">
    {/* Hero 内容 */}
  </div>
</section>
```

### 2. 加大圆角

将默认圆角替换为更大的值，营造柔和、卡通的动漫感：

- 卡片：`rounded-2xl`（16px）或 `rounded-3xl`（24px）
- 按钮：`rounded-xl`（12px）或 `rounded-2xl`（16px）
- 头像：`rounded-full`（圆形）或 `rounded-2xl`（方形大圆角）
- 输入框：`rounded-xl`
- 图片容器：`rounded-2xl` 或 `rounded-3xl`

```tsx
// 示例：动漫风格卡片
<div className="rounded-3xl bg-white shadow-lg overflow-hidden">
  <img src="..." className="w-full h-48 object-cover" />
  <div className="p-6">{/* 内容 */}</div>
</div>
```

### 3. 其他区域使用动漫背景

- 功能卡片、侧边栏、Footer 等区域可用竖图或横图作为装饰背景
- 作为分割线之间的过渡背景区域
- 图片只需局部展示（如半高），不需要占满整个区域

### 4. 头像使用动漫头像

- 用户头像、评论区头像、作者头像统一使用"图片资源"表中的头像 URL
- 默认选主头像 01 作为主头像，其余 7 张随机分配给不同用户
- 使用 `rounded-full` 圆形裁剪，或 `rounded-2xl` 方形大圆角

```tsx
// 示例：动漫头像
<img
  src="http://101.96.214.171:40027/i/2026/06/14/6a2e7136667d7.webp"
  alt="用户头像"
  className="w-12 h-12 rounded-full object-cover"
/>
```

### 5. 全局风格建议

- **配色**：倾向使用粉色系（`#f472b6`）、紫色系（`#a855f7`）、天蓝色系（`#38bdf8`）等明快色调；若项目已有强品牌色，作为点缀色叠加使用（如按钮 hover、徽章、进度条），不整体替换主色
- **字体**：可使用圆体/卡通风格字体增加动漫感
- **阴影**：使用彩色阴影（如 `shadow-pink-200/50`）替代默认灰色阴影
- **装饰元素**：可适当添加樱花、星星等动漫常见装饰元素（CSS 绘制或 emoji）

### 6. 图标方案：Lucide

使用 [Lucide](https://lucide.dev/) 作为图标库。天然圆角描边、AI 训练数据覆盖广、框架无关。

> **注意**：CDN 引入时建议锁定版本号（如 `lucide@0.460.0`），避免 `@latest` 在升级后产生破坏性变更。

**纯 HTML（零依赖 CDN 方式，AI 编码最友好）：**

```html
<!-- 1. 引入 CDN（建议锁定版本） -->
<script src="https://unpkg.com/lucide@0.460.0"></script>

<!-- 2. 任何 HTML 元素加 data-lucide 属性即可 -->
<i data-lucide="heart" class="w-6 h-6 text-pink-400"></i>
<i data-lucide="star" class="w-5 h-5 fill-amber-400"></i>
<i data-lucide="search" class="w-5 h-5 text-gray-300"></i>

<!-- 3. 页面底部初始化一次 -->
<script>lucide.createIcons();</script>
```

**React：**

```tsx
import { Heart, Star, Search, Sparkles } from 'lucide-react';
<Heart className="w-6 h-6 text-pink-400" />
<Star className="w-5 h-5 fill-amber-400 text-amber-400" />
```

**Vue 3：**

```vue
import { Heart, Star } from 'lucide-vue-next';
<Heart class="w-6 h-6 text-pink-400" />
```

**常用图标映射（动漫风格常用）：**

| 图标名 | 用途 |
|--------|------|
| `heart` | 点赞、收藏 |
| `star` | 评分、收藏 |
| `sparkles` | AI 功能、特效点缀 |
| `zap` | 快速、闪电体验 |
| `brain` | AI 智能 |
| `bot` | AI 助手、聊天机器人 |
| `rocket` | 启动、新产品发布 |
| `shield-check` | 安全、隐私保护 |
| `mic` | 语音交互 |
| `image` | 图片处理 |
| `message-square` | 聊天、消息 |
| `arrow-right` | 了解更多、下一步 |
| `chevron-down` | 下拉、滚动提示 |
| `cpu` | 端侧芯片、算力 |
| `calendar` | 预约、日期 |
| `info` | 关于 |
| `shield` | 隐私 |
| `mail` | 联系 |

AI 编码时只需记住图标名字符串，无需了解 SVG 实现细节。

### 7. 动画方案：AOS

使用 **AOS**（Animate on Scroll）为落地页添加滚动揭示动效。14KB，20+ 预设动画，框架无关，一个属性搞定。

> **注意**：不要用 Lenis 等平滑滚动库。macOS / iOS 触控板原生滚动已经是最佳体验，第三方平滑滚动会破坏惯性手感，反而变差。
>
> **与第 16 节"高斯模糊入场"配合时**：若 AOS 设置 `once: true`（推荐），元素只会动画一次，`blur-in` 不会反复触发，避免快速滚动时的闪烁问题。不要将 `once` 设为 `false` 与 `blur-in` 一起使用。

**AOS 快速集成（建议锁定版本）：**

```html
<!-- 引入 -->
<link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet">
<script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>

<!-- 初始化 -->
<script>
  AOS.init({ offset: 80, duration: 600, easing: 'ease-out-cubic', once: true });
</script>
```

只需给 HTML 元素添加 `data-aos` 属性：

```html
<div data-aos="fade-up">淡入上浮</div>
<div data-aos="fade-right" data-aos-delay="200">延迟 200ms 从右滑入</div>
<div data-aos="zoom-in" data-aos-duration="800">缩放入场</div>
<div data-aos="flip-left">翻转</div>
```

**常用动画映射（落地页标准配置）：**

| 区域 | 动画 | 延迟 |
|------|------|------|
| Hero 徽章标签 | `fade-down` | 0 |
| Hero 标题 | `fade-up` | 200ms |
| Hero 描述 | `fade-up` | 400ms |
| Hero 按钮 | `fade-up` | 600ms |
| 区块标题 | `fade-up` | 0 |
| 功能卡片（1/2/3） | `fade-up` | 100/250/400ms |
| 展示区-左内容 | `fade-right` | 0 |
| 展示区-右图 | `fade-left` | 200ms |
| 头像群（逐个） | `zoom-in` | 80ms 递增 |
| 评价卡片 | `fade-up` | 0/150/300ms |
| CTA 区域 | `fade-up` | 0 |

### 8. 背景图像视差

CSS `background-attachment: fixed` 让背景图相对视口固定，内容滚动时产生经典视差效果。每个 section 独立使用，无需 JS。

> **重要兼容性问题**：iOS Safari（以及部分移动 Chrome）对 `background-attachment: fixed` 支持差或完全不生效。**必须提供移动端 fallback**：用媒体查询在窄屏下移除 `bg-fixed`，退化为普通 `bg-scroll`，否则移动端背景图可能不显示或位置错乱。

**Tailwind 实现：**

给 section 加 `bg-fixed bg-cover bg-center`，用 inline style 设置 `background-image`，并添加移动端 fallback：

```html
<!-- Hero -->
<section class="relative min-h-screen flex items-center justify-center overflow-hidden bg-cover bg-center md:bg-fixed"
         style="background-image: url('http://101.96.214.171:40027/i/2026/06/14/6a2e74194f0f7.webp');">
  <div class="absolute inset-0 bg-black/50"></div>
  <div class="relative z-10">
    <h1>标题</h1>
  </div>
</section>

<!-- 另一个 section，独立背景 -->
<section class="relative py-24 px-4 overflow-hidden bg-cover bg-center md:bg-fixed"
         style="background-image: url('http://101.96.214.171:40027/i/2026/06/14/6a2e7415e0bd7.webp');">
  <div class="absolute inset-0 bg-purple-950/60"></div>
  <div class="relative z-10">
    <!-- 内容 -->
  </div>
</section>
```

每个 section 设置不同的背景图 URL，叠加半透明遮罩（`absolute inset-0 bg-xxx/xx`），内容放 `relative z-10` 内。`md:bg-fixed` 仅在桌面端（≥768px）启用视差，移动端保持默认 `bg-scroll`，避免兼容问题。

### 9. 视差滚动

JS `translate3d` 驱动 `<img>` 元素按不同速度偏移，实现多层深度视差滚动。每个 section 独立控制速度，灵活度高于 `bg-fixed`，且移动端兼容性更好。

> 适合需要多速度层级、移动端兼容、或背景图需要独立动画控制的场景。这是第 8 节 `bg-fixed` 在移动端失效时的更可靠替代方案。

**CSS：**

```css
.parallax-img {
  position: absolute;
  top: 0; left: 0;
  width: 100%;
  height: calc(100% + 200px);
  object-fit: cover;
  will-change: transform;
}
```

**HTML：**

```html
<section class="relative min-h-screen overflow-hidden">
  <img src="http://101.96.214.171:40027/i/2026/06/14/6a2e74194f0f7.webp"
       class="parallax-img" data-parallax-speed="0.3" />
  <div class="absolute inset-0 bg-black/40"></div>
  <div class="relative z-10">
    <!-- 内容 -->
  </div>
</section>
```

**JS：**

```js
const parallaxImages = document.querySelectorAll('.parallax-img');
function updateParallax() {
  const vh = innerHeight;
  parallaxImages.forEach(img => {
    const speed = parseFloat(img.dataset.parallaxSpeed) || 0.3;
    const section = img.parentElement;
    const rect = section.getBoundingClientRect();
    if (rect.bottom < 0 || rect.top > vh) return;
    const offset = ((rect.top + rect.height / 2) / vh - 0.5) * 100 * speed;
    img.style.transform = `translate3d(0, ${-offset}px, 0)`;
  });
}
window.addEventListener('scroll', () => requestAnimationFrame(updateParallax), { passive: true });
updateParallax();
```

**速度参考：**

| `data-parallax-speed` | 效果 |
|:--:|------|
| `0.1` | 几乎固定，远山感 |
| `0.3` | Hero 大图，微妙深度 |
| `0.5` | 明显漂移 |
| `0.8` | 快速移动，紧张动感 |

> **选择指南**：桌面端优先用 `bg-fixed` + `md:` 前缀（零 JS，简单），移动端兼容或多速度层级需求用 `translate3d` 方案（第 9 节）。

### 10. 打字机效果：typewriter-effect

使用 [typewriter-effect](https://www.npmjs.com/package/typewriter-effect)（12 万周下载，MIT，~5KB）实现逐字打印效果。零依赖，API 成熟可靠。

> **不要自己写 CSS `steps()` / `clip` 伪打字效果**，它只是裁剪已存在的文字，不是真正的逐字追加。

**CDN 引入（建议锁定版本）：**

```html
<script src="https://unpkg.com/typewriter-effect@2.21.0/dist/core.js"></script>
```

**HTML：**

```html
<span id="typewriter"></span>
```

**JS 初始化：**

```js
new Typewriter('#typewriter', {
  strings: ['从拍照修图到语音助手，AI 触手可及。'],
  autoStart: true,
  loop: true,         // 循环：打完 → 删除 → 再打
  delay: 60,          // 打字速度
  deleteSpeed: 30,    // 删除速度
  pauseFor: 3000,     // 打完暂停 3 秒再删
  cursor: '|',
  cursorClassName: 'text-pink-400',
});
```

**常用配置：**

| 参数 | 默认值 | 说明 |
|------|--------|------|
| `strings` | `[]` | 要打的文字数组 |
| `autoStart` | `false` | 自动开始 |
| `loop` | `false` | 是否循环 |
| `delay` | `auto` | 打字速度，60~80 适中 |
| `deleteSpeed` | `auto` | 删除速度，40 流畅 |
| `pauseFor` | — | 打完暂停多久（ms）。循环模式设 2000~3000，打完停一阵再删，视觉自然 |
| `cursor` | `'|'` | 光标字符 |
| `cursorClassName` | — | 光标 CSS 类名 |

### 11. 数字递增：CountUp.js

使用 [CountUp.js](https://inorganik.github.io/countUp.js/)（7500+ Star，零依赖，~5KB）实现数字滚到目标值。自带 `enableScrollSpy` 进入视野自动触发。

> **不要手写 IntersectionObserver + requestAnimationFrame**，CountUp.js 已完美处理缓动、滚动检测、千分位分隔符。

**CDN 引入（建议锁定版本）：**

```html
<script src="https://unpkg.com/countup.js@2.8.0/dist/countUp.umd.js"></script>
```

**HTML：**

```html
<span id="countUsers">0</span>
<span id="countRate">0</span>
<span id="countSpeed">0</span>
```

**JS 初始化：**

```js
new countUp.CountUp('countUsers', 500, { suffix: '万+', duration: 2.5, enableScrollSpy: true });
new countUp.CountUp('countRate', 99, { suffix: '%', duration: 2, enableScrollSpy: true });
new countUp.CountUp('countSpeed', 30, { suffix: 'ms', duration: 2, enableScrollSpy: true });
```

**常用配置：**

| 参数 | 默认值 | 说明 |
|------|--------|------|
| `suffix` | `''` | 后缀（万+、%、ms 等） |
| `prefix` | `''` | 前缀（$、¥ 等） |
| `duration` | `2` | 动画时长（秒） |
| `enableScrollSpy` | `false` | 进入视野自动触发 |
| `separator` | `','` | 千分位分隔符 |
| `decimal` | `'.'` | 小数点字符 |
| `useEasing` | `true` | 智能缓动 |

### 12. 滚动进度条

页面顶部一根渐变色进度条，实时反映滚动位置。纯 JS 5 行，零依赖。

**CSS：**

```css
#scroll-progress {
  position: fixed;
  top: 0; left: 0;
  height: 3px;
  background: linear-gradient(90deg, #f472b6, #a855f7, #38bdf8);
  z-index: 100;
  width: 0%;
  transition: width 0.1s linear;
}
```

**HTML：**

```html
<div id="scroll-progress"></div>
```

**JS（放在 `</body>` 前）：**

```js
window.addEventListener('scroll', () => {
  const pct = (scrollY / (document.body.scrollHeight - innerHeight)) * 100;
  document.getElementById('scroll-progress').style.width = pct + '%';
}, { passive: true });
```

### 13. SVG 描边动画

SVG 路径像被手绘出来一样，逐段显示。CSS `stroke-dashoffset` 动画 + IntersectionObserver。**每次进入视口重新绘制，滚出时重置**，绘制完成后加呼吸光效保持动态感。

**原理**：SVG `path` 设置 `stroke-dasharray` 和 `stroke-dashoffset`（等于路径总长），通过 CSS 动画把 `stroke-dashoffset` 降到 0，路径逐段"画"出来。

> **关键**：`stroke-dasharray` / `--len` 的值必须等于该 `path` 的实际周长（`path.getTotalLength()`），不能凭感觉填数字——否则动画起点/终点会有跳变或残留线段。生成 SVG 后，在浏览器控制台对每个 `path` 运行 `el.getTotalLength()` 获取真实长度，再填入 CSS。下方示例中的数值（`40`、`600`）仅为占位示例，必须替换为实测值。

**CSS：**

```css
.draw-line {
  stroke-dasharray: var(--len);
  stroke-dashoffset: var(--len);
}
.draw-line.animate {
  animation: draw 1.8s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
}
/* 绘制完成后呼吸光效，保持动态感 */
.draw-line.animate-done {
  stroke-dashoffset: 0;
  animation: glowPulse 3s ease-in-out infinite;
}
@keyframes draw {
  to { stroke-dashoffset: 0; }
}
@keyframes glowPulse {
  0%, 100% { filter: drop-shadow(0 0 2px rgba(168,85,247,0.3)); }
  50%      { filter: drop-shadow(0 0 8px rgba(168,85,247,0.7)); }
}
```

**HTML（带梯度波纹分隔线 + 星星，数值需用实测 `getTotalLength()` 替换）：**

```html
<div class="svg-divider flex justify-center py-8">
  <svg viewBox="0 0 672 24" fill="none">
    <!-- 左边星：stroke-dasharray/dashoffset 需替换为实测路径长度 -->
    <path class="draw-star" d="M12 2l2 6h6l-5 4 2 6-5-4-5 4 2-6-5-4h6z"
      stroke="url(#g)" stroke-width="2" stroke-dasharray="<实测长度>" stroke-dashoffset="<实测长度>" />
    <!-- 中间波浪：--len 需替换为实测路径长度 -->
    <path class="draw-line" style="--len: <实测长度>;"
      d="M48 12 Q96 0 144 12 Q192 24 240 12 Q288 0 336 12 Q384 24 432 12 Q480 0 528 12 Q576 24 624 12"
      stroke="url(#g)" stroke-width="2" stroke-linecap="round" />
    <!-- 右边星 -->
    <path class="draw-star" d="M660 2l2 6h6l-5 4 2 6-5-4-5 4 2-6-5-4h6z"
      stroke="url(#g)" stroke-width="2" stroke-dasharray="<实测长度>" stroke-dashoffset="<实测长度>" />
    <defs>
      <linearGradient id="g" x1="0" y1="0" x2="1" y2="0">
        <stop stop-color="#f472b6" /><stop offset="0.5" stop-color="#a855f7" /><stop offset="1" stop-color="#38bdf8" />
      </linearGradient>
    </defs>
  </svg>
</div>
```

**或：用 JS 自动获取路径长度（推荐，避免手动测量出错）：**

```js
// 页面加载后自动设置每个 path 的 dasharray/dashoffset
document.querySelectorAll('.draw-line, .draw-star').forEach(path => {
  const len = path.getTotalLength();
  path.style.setProperty('--len', len);
  path.style.strokeDasharray = len;
  path.style.strokeDashoffset = len;
});
```

**JS 触发（进入绘制 / 离开重置）：**

```js
const drawObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    const svg = entry.target;
    const lines = svg.querySelectorAll('.draw-line, .draw-star');
    if (entry.isIntersecting) {
      // 移除旧状态，强制回流后重绘
      lines.forEach(el => el.classList.remove('animate', 'animate-done'));
      void svg.offsetWidth;
      lines.forEach(el => el.classList.add('animate'));
      // 绘制完成后切换为呼吸光效
      setTimeout(() => {
        lines.forEach(el => {
          el.classList.remove('animate');
          el.classList.add('animate-done');
        });
      }, 1900);
    } else {
      // 滚出视口时重置
      lines.forEach(el => el.classList.remove('animate', 'animate-done'));
    }
  });
}, { threshold: 0.3 });
drawObserver.observe(document.querySelector('.svg-divider'));
```

> **关键点**：
> - `stroke-dasharray` / `--len` 必须等于实际路径长度（用 `getTotalLength()` 获取，或用上面的自动化脚本），否则会出现跳变或残留线段
> - `animate-done` 呼吸光效（`glowPulse`）让绘制完成后仍有动态感
> - 进入时先 `remove` 再 `add` 类名，配合 `void svg.offsetWidth` 强制回流，保证每次都能重新触发动画
> - 离开时重置所有类名，下次进入即重新绘制

### 14. 鼠标跟随光晕

卡片 hover 时，`radial-gradient` 光晕跟随鼠标移动，营造强烈的科技感和互动性。纯 CSS + 15 行 JS。

**CSS：**

```css
.glow-card {
  position: relative;
  overflow: hidden;
}
.glow-card::before {
  content: '';
  position: absolute;
  inset: 0;
  z-index: 1;
  pointer-events: none;
  opacity: 0;
  background: radial-gradient(600px circle at var(--mx, 50%) var(--my, 50%), rgba(168,85,247,0.15), transparent 40%);
  transition: opacity 0.3s;
}
.glow-card:hover::before {
  opacity: 1;
}
.glow-card > * {
  position: relative;
  z-index: 2;
}
```

**HTML（给卡片加 `glow-card` 类）：**

```html
<div class="card-hover glow-card rounded-3xl bg-gradient-to-br from-gray-900 to-gray-800 border border-gray-700/50 overflow-hidden">
  <!-- 卡片内容 -->
</div>
```

**JS（15 行）：**

```js
document.querySelectorAll('.glow-card').forEach(card => {
  card.addEventListener('mousemove', e => {
    const rect = card.getBoundingClientRect();
    card.style.setProperty('--mx', (e.clientX - rect.left) + 'px');
    card.style.setProperty('--my', (e.clientY - rect.top) + 'px');
  });
  card.addEventListener('mouseleave', () => {
    card.style.removeProperty('--mx');
    card.style.removeProperty('--my');
  });
});
```

> **原理**：CSS 自定义属性 `--mx` / `--my` 实时更新光晕中心位置。`radial-gradient` 的 `circle at` 读取这两个变量。`pointer-events: none` 确保 `::before` 不拦截鼠标事件。`> * { z-index: 2 }` 保证内容在光晕上方。`mouseleave` 时移除属性，光晕回到默认位置。

### 15. 无限横向跑马灯

使用 [Embla Carousel](https://www.embla-carousel.com/)（6K+ stars，~10KB）的 `autoplay` 插件实现无限横向滚动。适合品牌 Logo 墙。

> **关键前提**：Logo 总数必须足够多，使 container 宽度超过 viewport 宽度，Embla 才有溢出空间可滚动。**15 个以上为宜**。
>
> **若可用条目不足 15 个**：将现有条目数组**复制拼接 2-3 次**后再渲染（如 `[...items, ...items, ...items]`），凑够溢出宽度；不要强行用不足的条目数走跑马灯效果，否则 `loop: true` 会因无溢出空间而不滚动或跳动。

**CDN 引入（建议锁定版本）：**

```html
<script src="https://unpkg.com/embla-carousel@8/embla-carousel.umd.js"></script>
<script src="https://unpkg.com/embla-carousel-autoplay@8/embla-carousel-autoplay.umd.js"></script>
```

**CSS：**

```css
.embla {
  overflow: hidden;
}
.embla__viewport {
  overflow: hidden;
}
.embla__container {
  display: flex;
  touch-action: pan-y pinch-zoom;
}
.embla__slide {
  flex: 0 0 auto;
  min-width: 0;
  padding: 0 1.5rem;
}
.marquee-item {
  display: flex;
  align-items: center;
  white-space: nowrap;
  font-size: 0.95rem;
  font-weight: 600;
  color: #9ca3af;
  user-select: none;
}
```

**HTML（15+ 个 Logo 确保溢出，不足时复制拼接）：**

```html
<section class="py-16 bg-gray-950/50 border-y border-gray-800/30 embla">
  <div class="embla__viewport">
    <div class="embla__container">
      <div class="embla__slide"><span class="marquee-item"><i data-lucide="cpu"></i>LLaMA</span></div>
      <div class="embla__slide"><span class="marquee-item"><i data-lucide="sparkles"></i>Gemini</span></div>
      <!-- ... 至少 15 个，不足则复制现有条目拼接 ... -->
    </div>
  </div>
</section>
```

**JS 初始化（放在 `lucide.createIcons()` 之后）：**

```js
lucide.createIcons();

const emblaNode = document.querySelector('.embla');
if (emblaNode) {
  EmblaCarousel(
    emblaNode.querySelector('.embla__viewport'),
    { align: 'start', loop: true, duration: 50 },
    [EmblaCarouselAutoplay({ delay: 4000, stopOnInteraction: false })]
  );
}
```

**参数说明：**

| 参数 | 值 | 说明 |
|---|---|---|
| `align` | `'start'` | 从起始位置对齐，避免居中导致空白 |
| `loop` | `true` | 无限循环 |
| `delay` | `4000` | 每个 slide 展示时间 (ms)，值越大越慢 |
| `stopOnInteraction` | `false` | 拖拽后不停止 |
| `duration` | `50` | 过渡动画时长 (ms)，越小过渡越快 |

> **关键点**：
> - 必须保证 container 宽度 > viewport 宽度，否则无法滚动。15 个以上 Logo 为宜，不足则复制拼接
> - `delay: 4000` 控制滚动速度，值越大越慢，配合短 `duration` 过渡流畅
> - `flex: 0 0 auto` 保持每个 Logo 自身宽度
> - `touch-action: pan-y pinch-zoom` 按官方规范，防止触屏冲突

### 16. 高斯模糊入场

搭配 AOS，元素进入视口时从 `filter: blur(12px)` + `opacity: 0` 过渡到清晰可见。纯 CSS transition，AOS 负责触发。

> **前提**：AOS 必须以 `once: true` 初始化（见第 7 节），否则元素反复进出视口会导致 `blur-in` 反复触发，产生闪烁。

**CSS（与 AOS 配合）：**

```css
/* 初始状态：模糊 + 透明 */
.blur-in {
  filter: blur(12px);
  opacity: 0;
  transition: filter 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94),
              opacity 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
/* AOS 进入视口后通过 .aos-animate 完成过渡 */
.blur-in.aos-animate {
  filter: blur(0);
  opacity: 1;
}
```

**HTML（`blur-in` + `data-aos` 配对使用）：**

```html
<div data-aos="fade-right" data-aos-duration="1000" class="blur-in">
  <h2>标题</h2>
  <p>内容</p>
</div>

<img src="http://101.96.214.171:40027/i/2026/06/15/6a2eef614e150.jpg" class="blur-in" data-aos="fade-left" data-aos-duration="1000" />

<!-- 级联延迟 -->
<div class="blur-in" data-aos="fade-up" data-aos-duration="600" data-aos-delay="200">第 1 项</div>
<div class="blur-in" data-aos="fade-up" data-aos-duration="600" data-aos-delay="400">第 2 项</div>
<div class="blur-in" data-aos="fade-up" data-aos-duration="600" data-aos-delay="600">第 3 项</div>
```

> **原理**：AOS 滚动到元素位置时添加 `.aos-animate` 类，CSS transition 接管实际的视觉属性变化。`blur-in` 只定义起始/结束状态和过渡曲线，不写 `@keyframes`。`data-aos-delay` 配合不同 delay 实现级联入场，逐个从模糊变清晰。`once: true` 确保动画只触发一次，避免闪烁。

### 17. Mermaid 图表 / 流程图

用 [Mermaid](https://mermaid.js.org/) 在页面内渲染流程图、时序图、状态图等。**主题用内置 `dark` 即可**，不要额外叠浅色背景或自定义亮色主题，与动漫暗色页面更协调。

> **展示空间（重要）**：Mermaid 在窄容器里会被压得很小，但也不要为了「够大」而无限放大。目标是**文字清晰可读、布局不拥挤**——给图表独立全宽区块即可，尺寸随内容自适应，简单图不必强行撑高。

**CDN 快速集成（建议锁定版本）：**

```html
<!-- 1. 引入 -->
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
  mermaid.initialize({
    startOnLoad: true,
    theme: 'dark',           // 默认暗色，无需再改 background
    securityLevel: 'loose',
    flowchart: {
      useMaxWidth: true,     // 默认 true：随容器等比缩放，简单图不会撑爆
      htmlLabels: true,
      padding: 16,
      nodeSpacing: 40,
      rankSpacing: 48,
    },
    themeVariables: {
      fontSize: '15px',
    },
  });
</script>

<!-- 2. 图表容器：留足宽高 -->
<section class="mermaid-section">
  <div class="mermaid-wrap">
    <pre class="mermaid">
flowchart LR
  A[用户访问] --> B{已登录?}
  B -->|是| C[进入首页]
  B -->|否| D[跳转登录]
  C --> E[浏览内容]
  D --> E
    </pre>
  </div>
</section>
```

**CSS（可读即可，勿强行撑大）：**

```css
/* 独立区块，不要嵌在窄列 grid 里 */
.mermaid-section {
  width: 100%;
  margin: 2rem 0;
}

.mermaid-wrap {
  width: 100%;
  padding: 1.25rem 1.5rem;
  border-radius: 1rem;
  overflow-x: auto;           /* 极宽图可横向滚动 */
}

/* 随容器缩放，上限不超过内容区宽度 */
.mermaid-wrap svg {
  display: block;
  margin: 0 auto;
  max-width: 100%;
  height: auto;
}
```

**何时需要更大：**

| 情况 | 做法 |
|------|------|
| 简单流程（≤6 节点） | 保持默认 `useMaxWidth: true`，不设 `min-height` |
| 复杂架构图（多 subgraph） | 容器设 `min-height: 280px`，或单图 init 里设 `useMaxWidth: false` |
| 被压得太小 | 先检查是否嵌在 `max-w-sm` / 双列 grid；改全宽通常比关 `useMaxWidth` 更有效 |
| 被放得太大 | 去掉 `max-width: none`、`min-width: 640px` 等 CSS；间距回调到默认 |

**布局建议：**

| 场景 | 做法 |
|------|------|
| 落地页 / 文档页主内容 | 单独一行全宽（`w-full`），不要和侧边栏并排 |
| 卡片内嵌小图 | 仅适合 3 节点以内的极简图；否则拆到弹层或独立 section |
| 移动端 | 保留 `overflow-x: auto` |
| 多图并列 | 用纵向堆叠，不要用 `grid-cols-2` 把两个流程图挤在一行 |

**单图覆盖配置（可选，写在 diagram 开头）：**

```html
<div class="mermaid-wrap">
  <pre class="mermaid">
%%{init: {'theme': 'dark', 'flowchart': {'useMaxWidth': true}}}%%
sequenceDiagram
  participant U as 用户
  participant A as 前端
  participant S as 服务端
  U->>A: 点击提交
  A->>S: POST /api/form
  S-->>A: 200 OK
  A-->>U: 成功提示
  </pre>
</div>
```

**React（`@mermaid-js/mermaid` 或动态 import）：**

```tsx
'use client';
import { useEffect, useRef } from 'react';

const MERMAID_CONFIG = {
  startOnLoad: false,
  theme: 'dark',
  flowchart: { useMaxWidth: true, nodeSpacing: 40, rankSpacing: 48 },
  themeVariables: { fontSize: '15px' },
};

export function MermaidBlock({ chart }: { chart: string }) {
  const ref = useRef<HTMLDivElement>(null);

  useEffect(() => {
    let cancelled = false;
    (async () => {
      const mermaid = (await import('mermaid')).default;
      mermaid.initialize(MERMAID_CONFIG);
      if (!ref.current || cancelled) return;
      const { svg } = await mermaid.render(`mmd-${Date.now()}`, chart);
      ref.current.innerHTML = svg;
    })();
    return () => { cancelled = true; };
  }, [chart]);

  return (
    <section className="mermaid-section w-full my-8">
      <div className="mermaid-wrap px-6 py-5 rounded-2xl overflow-x-auto">
        <div ref={ref} className="[&>svg]:mx-auto [&>svg]:max-w-full [&>svg]:h-auto" />
      </div>
    </section>
  );
}
```

**常用图类型速查：**

| 语法关键字 | 用途 |
|-----------|------|
| `flowchart TD` / `LR` | 业务流程、架构流向 |
| `sequenceDiagram` | 接口调用、交互时序 |
| `stateDiagram-v2` | 状态机、订单/任务状态 |
| `classDiagram` | 模块关系（技术文档） |
| `gantt` | 排期、里程碑 |

> **关键点**：
> - **主题**：只用 `theme: 'dark'`，不额外铺白底或 `bg-white`
> - **尺寸**：默认 `useMaxWidth: true` + `max-width: 100%`，简单图随容器缩放；复杂宽图才考虑关 `useMaxWidth` 或设 `min-height`
> - **节点数量**：单图超过 8–10 个节点时考虑拆成多图或子图（`subgraph`），避免一屏塞满
> - **与 AOS 配合**：图表容器可加 `data-aos="fade-up"`，但不要用 `blur-in`（模糊滤镜可能影响 SVG 清晰度）
