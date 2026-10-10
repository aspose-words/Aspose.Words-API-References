---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize 方法"
linktitle: "RenderToSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize 方法。将形状渲染到 Graphics 对象中，指定大小（C++）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


将形状渲染到 **Graphics** 对象，使用指定的大小。

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | 要渲染到的对象。 |
| x | float | 已渲染形状左上角的 X 坐标（以世界单位计）。 |
| y | float | 已渲染形状左上角的 Y 坐标（以世界单位计）。 |
| width | float | 渲染形状可以占用的最大宽度（以世界单位计）。 |
| height | float | 渲染形状可以占用的最大高度（以世界单位计）。 |

### ReturnValue

为使渲染形状适应指定大小而自动计算的比例。

## 另见

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
