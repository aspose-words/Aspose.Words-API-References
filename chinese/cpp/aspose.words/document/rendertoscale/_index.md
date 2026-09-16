---
title: "Aspose::Words::Document::RenderToScale 方法"
linktitle: "RenderToScale"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::RenderToScale 方法。将文档页面渲染到 Graphics 对象，并按指定比例缩放（C++）。"
type: docs
weight: 70000
url: /zh/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


将文档页面渲染到 **Graphics** 对象，使用指定的比例。

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int32_t | 基于 0 的页面索引。 |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | 要渲染到的对象。 |
| x | float | 渲染页面左上角的 X 坐标（以世界单位计） |
| y | float | 渲染页面左上角的 Y 坐标（以世界单位计） |
| scale | float | 渲染页面的比例（1.0 表示 100%） |

### ReturnValue

渲染页面的宽度和高度（以世界单位计）

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
