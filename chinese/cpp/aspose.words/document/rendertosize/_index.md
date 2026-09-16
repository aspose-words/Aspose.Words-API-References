---
title: "Aspose::Words::Document::RenderToSize 方法"
linktitle: "RenderToSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::RenderToSize 方法。将文档页面渲染到 Graphics 对象中，以指定的大小（C++）。"
type: docs
weight: 71000
url: /zh/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


将文档页面渲染到 **Graphics** 对象，使用指定的尺寸。

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int32_t | 基于 0 的页面索引。 |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | 要渲染到的对象。 |
| x | float | 渲染页面左上角的 X 坐标（以世界单位计） |
| y | float | 渲染页面左上角的 Y 坐标（以世界单位计） |
| width | float | 渲染页面可占用的最大宽度（以世界单位计）。 |
| height | float | 渲染页面可占用的最大高度（以世界单位计）。 |

### ReturnValue

为使渲染页面适应指定大小而自动计算的比例。

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
