---
title: "Aspose::Words::Saving::MetafileRenderingMode 枚举"
linktitle: "MetafileRenderingMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MetafileRenderingMode 枚举。指定 Aspose.Words 在 C++ 中应如何渲染 WMF 和 EMF 元文件。"
type: docs
weight: 69000
url: /zh/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


指定 Aspose.Words 应如何呈现 WMF 和 EMF 元文件。

```cpp
enum class MetafileRenderingMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words 尝试将元文件渲染为矢量图形。如果 Aspose.Words 无法将某些元文件记录正确渲染为矢量图形，则 Aspose.Words 会将该元文件渲染为位图。 |
| 矢量 | 1 | Aspose.Words 将元文件渲染为矢量图形。 |
| 位图 | 2 | Aspose.Words 调用 GDI+ 将元文件渲染为位图，然后将位图保存到输出文档中。 |

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
