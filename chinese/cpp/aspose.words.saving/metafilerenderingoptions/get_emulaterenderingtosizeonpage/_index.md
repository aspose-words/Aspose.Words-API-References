---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage 方法"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage 方法。获取或设置一个值，决定元文件渲染是根据页面上的大小模拟显示元文件，还是以默认大小显示元文件（C++）。"
type: docs
weight: 4334
url: /zh/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


获取或设置决定元文件渲染是根据页面尺寸模拟元文件显示还是使用默认尺寸显示的值。

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## 备注


当元文件在 MS Word 中显示时，某些图形可能会根据实际的像素大小进行缩放。也就是说，即使是缩放操作也可能影响元文件的显示。

当此值设置为 **true** 时，Aspose.Words 会根据页面上的元文件大小模拟渲染。像素大小是根据页面上的元文件大小和指定的 [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/) 计算得出的。

当此值设置为 **false** 时，Aspose.Words 会将元文件渲染模拟为其默认的像素大小。

此选项仅在元文件被渲染为矢量图形时使用。

默认值为 **true**。
## 另见

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
