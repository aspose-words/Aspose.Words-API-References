---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics 方法"
linktitle: "get_CacheBackgroundGraphics"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics 方法。获取或设置一个值，以确定是否在 C++ 中缓存放置在文档''的背景中的图形。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_cachebackgroundgraphics/
---
## PdfSaveOptions::get_CacheBackgroundGraphics method


获取或设置决定是否缓存放置在文档背景中的图形的值。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics() const
```

## 备注


默认值为 **true**，背景图形将作为 xObject 写入 PDF 文档。

当值为 **false** 时，背景图形不会被缓存。

某些形状不支持缓存（带有字段、书签、HRefs 的形状）。

[Document](../../../aspose.words/document/) background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page. 
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
