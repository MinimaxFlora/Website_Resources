# 图像资源

站点（<https://www.tatalvpai.vip>）用到的图片素材。按用途分目录存放，每个子目录自带 README。

## 目录结构

```
images/
├── README.md          ← 本文件
└── logo/              ← 品牌标识（完整说明见 logo/README.md）
    ├── README.md
    ├── logo.png       500×158   RGBA  浅色模式头部 logo
    ├── logo_dark.png  300×95    RGBA  深色 / 夜间模式头部 logo
    ├── favicon.ico    16/32/48/64     浏览器标签图标
    ├── favicon.png    64×64     透明底  备用图标
    ├── icon.png       148×148   浅底    桌面图标（iOS 添加到主屏幕）
    ├── icon-180.png   180×180   浅底    iPhone 标准尺寸
    └── icon-512.png   512×512   浅底    Android / PWA
```

## 品牌图一览

| 文件 | 尺寸 | 透明底 | 用途 |
| :-- | :-- | :--: | :-- |
| `logo/logo.png` | 500 × 158 | ✓ | 子比主题 `logo_src`（浅色头部） |
| `logo/logo_dark.png` | 300 × 95 | ✓ | 子比主题 `logo_src_dark`（深色头部） |
| `logo/favicon.ico` | 16 / 32 / 48 / 64 | ✓ | 浏览器标签页 |
| `logo/favicon.png` | 64 × 64 | ✓ | 旧浏览器 / 备用 |
| `logo/icon.png` | 148 × 148 | — | 桌面图标（iOS 主屏幕） |
| `logo/icon-180.png` | 180 × 180 | — | iPhone 标准尺寸 |
| `logo/icon-512.png` | 512 × 512 | — | Android / PWA |

尺寸与子比主题自带的 `img/logo.png`（500×158）、`img/logo_dark.png`（300×95）一致，
替换时**同名覆盖即可**，不需要改任何 CSS。

## 约定

1. **透明底**：品牌图一律用 RGBA PNG，不留白底/黑底，深浅两套主题都能用。
2. **尺寸对齐**：logo 宽高比固定 3.16:1，改图按 500×158 或等比例放大（1000×316、2000×632）。
3. **命名**：`xxx.png` 给浅色模式，`xxx_dark.png` 给深色模式，后缀不要乱改。
4. **新增文件**：同步更新上面的表格，写清尺寸和用途。

## 配色

| 用途 | 色值 |
| :-- | :-- |
| 主绿（图形块面） | `#1EC216` |
| 粉（JTGY 字标） | `#E56D96` |

## 直接引用

```
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/logo.png
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/logo_dark.png
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/favicon.ico
```

> 浏览器会缓存 favicon，换图标后按 `Ctrl/Cmd + Shift + R` 强制刷新。
