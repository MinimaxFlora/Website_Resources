# Website_Resources

站点 **[疆途光影](https://www.tatalvpai.vip)** 的静态资源仓库：品牌图、图标、以及后续的图片素材。

所有图片按用途分目录存放，规格与用法统一见本文。

## 目录

```
.
├── LICENSE
└── images/
    └── logo/                # 品牌标识
        ├── logo.png         500×158   RGBA  浅色头部 logo
        ├── logo_dark.png    300×95    RGBA  深色头部 logo
        ├── favicon.ico      16/32/48/64    浏览器标签图标
        ├── favicon.png      64×64     透明底  备用图标
        ├── icon.png         148×148   浅底    桌面图标（iOS 主屏幕）
        ├── icon-180.png     180×180   浅底    iPhone 标准尺寸
        └── icon-512.png     512×512   浅底    Android / PWA
```

## 品牌总览

| 资源 | 预览 | 规格 |
| :-- | :-- | :-- |
| 主 logo | ![logo](images/logo/logo.png) | 500×158，透明底，绿标 + 粉色 JTGY |
| 深色 logo | ![logo dark](images/logo/logo_dark.png) | 300×95，透明底，用于夜间模式 |
| 桌面图标 | ![icon](images/logo/icon.png) | 148×148，浅底 `#FBFBFB` |
| 标签图标 | ![favicon](images/logo/favicon.png) | 64×64，透明底 |

> 上面表格里的图片用的是仓库相对路径，在 GitHub 页面上会直接渲染出来。

## 规格速查

| 项目 | 值 |
| :-- | :-- |
| 主色（绿） | `#1EC216` |
| 辅色（粉） | `#E56D96` |
| logo 宽高比 | 3.16 : 1（500×158 / 1000×316） |
| 桌面图标留白 | 图形宽度占画布 53.2%，居中 |
| favicon | `.ico` 需含 16/32/48/64 四个尺寸 |

尺寸与子比主题自带的 `img/logo.png`、`img/logo_dark.png`、`img/icon.png` 一一对应，
替换时**同名覆盖**即可，不需要改 CSS。

## 直接引用

```
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/logo.png
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/logo_dark.png
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/favicon.ico
https://raw.githubusercontent.com/MinimaxFlora/Website_Resources/master/images/logo/icon.png
```

## 约定

- 品牌图一律 **RGBA 透明底**（桌面图标除外，用浅底）
- `xxx.png` 给浅色模式，`xxx_dark.png` 给深色模式，后缀不要改
- 新增文件请同步更新本文的表格

## 重制方法

从原稿 `images/logo/logo.png`（或更高的原始尺寸）出发：

1. 按绿色强度生成 alpha matte：`G - (R+B)/2`，把白色底转透明；
2. 深色版按与背景色 `#323337` 的 RGB 距离生成 alpha；
3. 等比缩放并居中到 500×158 / 300×95，保持贴边构图；
4. `.ico` 由 256×256 母版导出 16/32/48/64 四个尺寸；
5. 桌面图标按子比 `img/icon.png` 的构图重绘：浅底 `#FBFBFB`、图形宽占 53.2%、居中留白。

## 许可

仓库内的图形标识归 **疆途光影** 所有，仅用于本站及本站关联项目，未经许可请勿转载使用。
其余内容见 [LICENSE](LICENSE)。
