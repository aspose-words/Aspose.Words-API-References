---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf 方法"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf 方法。获取或设置决定在 C++ 中如何渲染包含嵌入式 EMF 元文件的 WMF 元文件的值。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


获取或设置一个值，用于确定如何呈现包含嵌入式 EMF 元文件的 WMF 元文件。

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## 备注


WMF 元文件可能包含嵌入的 EMF 数据。MS Word 在大多数情况下使用嵌入的 EMF 数据。GDI+ 总是使用 WMF 数据。

当此值设置为 **true** 时，Aspose.Words 在渲染时使用嵌入的 EMF 数据。

当此值设置为 **false** 时，Aspose.Words 在渲染时使用 WMF 数据。

此选项仅在元文件被渲染为矢量图形时使用。当元文件渲染为位图时，始终使用 WMF 数据。

默认值为 **true**。
## 另见

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
