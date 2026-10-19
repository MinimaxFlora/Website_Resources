# 品牌图像资源 · 疆途光影

站点 <https://www.tatalvpai.vip> 使用的全套品牌图，基于原 logo 提取重制。

## 文件

| 文件 | 尺寸 | 格式 | 用途 |
| :-- | :-- | :-- | :-- |
| `favicon.ico` | 16 / 32 / 48 / 64（多尺寸合一） | ICO | 浏览器标签页图标。子比建议 48×48 |
| `favicon.png` | 64 × 64 | PNG（透明底） | 部分场景 / 旧设备兜底 |
| `logo.png` | 500 × 158 | PNG（RGBA 透明底） | 浅色模式下站点头部 logo |
| `logo_dark.png` | 300 × 95 | PNG（RGBA 透明底） | 深色 / 夜间模式下的头部 logo |
| `icon.png` | 148 × 148 | PNG（浅底 `#FBFBFB`） | 桌面图标（iOS 添加到主屏幕） |
| `icon-180.png` | 180 × 180 | PNG（浅底 `#FBFBFB`） | iPhone 标准尺寸，iOS 优先取这个 |
| `icon-512.png` | 512 × 512 | PNG（浅底 `#FBFBFB`） | Android 桌面 / PWA / 商店图标 |

尺寸与透明通道均与子比主题自带的 `img/logo.png`（500×158）、`img/logo_dark.png`（300×95）一致，
替换时不需要改任何 CSS，直接同名覆盖即可。

## 设计说明

- **图形**：绿色块面 + 白色斜切，取自原 logo 的标记部分
- **配色**：绿 `#1EC216`，粉 `#E56D96`（与 JTGY 字标一致）
- **透明底**：白底 / 深灰底（`#323337`）已抠除，边缘 0.6px 羽化，缩放无白边
- **贴边构图**：图形铺满画布，与主题原图一致

## 在子比主题里怎么用

| 后台位置 | 对应文件 |
| :-- | :-- |
| 主题设置 → 全局 → 网站 logo | `logo.png` |
| 主题设置 → 全局 → 深色模式 logo | `logo_dark.png` |
| 主题设置 → 全局 → 网站图标（favicon） | `favicon.ico` |
| 主题设置 → 全局 → 桌面图标 / Apple Touch | `icon.png`（148×148） |

> 换 favicon 后浏览器会缓存旧图标，按 `Ctrl/Cmd + Shift + R` 强制刷新才能看到。

## 直接引用（raw 地址）

```
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/logo.png
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/logo_dark.png
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/favicon.ico
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/favicon.png
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/icon.png
```

## 重制方法

从 `images/logo.png` 级原稿出发：

1. 按绿色强度生成 alpha matte（`G - (R+B)/2`），把白色底转透明；
2. 深色版按与背景色 `#323337` 的 RGB 距离生成 alpha；
3. 等比缩放并居中到目标画布（500×158 / 300×95），保持贴边构图；
4. `.ico` 由 256×256 母版导出 16/32/48/64 四个尺寸；
5. 桌面图标按主题 `img/icon.png` 的构图重绘：浅底 `#FBFBFB`、图形宽度占画布 53.2%、居中留白，导出 148/180/512。
