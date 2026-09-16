---
title: "Aspose::Words::Saving::GraphicsQualityOptions::get_UseTileFlipMode 方法"
linktitle: "get_UseTileFlipMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::GraphicsQualityOptions::get_UseTileFlipMode 方法。获取或设置一个标志，指示 WrapMode 是否为 TileFlipXY（C++）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.saving/graphicsqualityoptions/get_usetileflipmode/
---
## GraphicsQualityOptions::get_UseTileFlipMode method


获取或设置指示 WrapMode 是否为 TileFlipXY 的标志。

```cpp
bool Aspose::Words::Saving::GraphicsQualityOptions::get_UseTileFlipMode() const
```

## 备注


该 **WrapMode** 指定当纹理或渐变小于填充区域时的平铺方式。

默认使用 **Tile**（指定不翻转的平铺）。这会导致缩放图像（高分辨率）渲染不准确。

此属性允许将 WrapMode 切换为 **TileFlipXY**（指定在沿行移动时水平翻转瓦片，在沿列移动时垂直翻转瓦片）。
## 另见

* Class [GraphicsQualityOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
