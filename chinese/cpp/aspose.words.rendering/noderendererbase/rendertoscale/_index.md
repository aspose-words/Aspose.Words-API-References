---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToScale 方法"
linktitle: "RenderToScale"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToScale 方法。将在 C++ 中将形状渲染到 Graphics 对象的指定比例。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


将形状渲染到 **Graphics** 对象，使用指定的比例。

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | 要渲染到的对象。 |
| x | float | 已渲染形状左上角的 X 坐标（以世界单位计）。 |
| y | float | 已渲染形状左上角的 Y 坐标（以世界单位计）。 |
| scale | float | 渲染形状的比例（1.0 表示 100%）。 |

### ReturnValue

已渲染形状的宽度和高度（以世界单位计）。

## 另见

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
