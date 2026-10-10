---
title: "Aspose::Words::Rendering::ShapeRenderer class"
linktitle: "ShapeRenderer"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::ShapeRenderer 类。提供将单个 Shape 或 GroupShape 渲染为光栅或矢量图像或渲染到 Graphics 对象的方法。欲了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


提供将单个 [Shape](../../aspose.words.drawing/shape/) 或 [GroupShape](../../aspose.words.drawing/groupshape/) 渲染为光栅或矢量图像或渲染到 Graphics 对象的方法。欲了解更多，请访问 [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) 文档文章。

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | 获取形状的实际边界（以点为单位）。 |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | 获取形状的不透明边界（以点为单位）。 |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | 获取形状的实际大小（以点为单位）。 |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | 根据指定的缩放因子和分辨率计算形状的像素边界。 |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | 根据指定的缩放因子和分辨率计算形状的像素边界。 |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | 根据指定的缩放因子和分辨率计算形状的不透明像素边界。 |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | 根据指定的缩放因子和分辨率计算形状的不透明像素边界。 |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | 根据指定的缩放因子和分辨率计算形状的像素大小。 |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | 根据指定的缩放因子和分辨率计算形状的像素大小。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | 将形状渲染到 **Graphics** 对象，使用指定的比例。 |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | 将形状渲染到 **Graphics** 对象，使用指定的大小。 |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | 将形状渲染为图像并保存到文件。 |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | 将形状渲染为 SVG 图像并保存到文件。 |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | 将形状渲染为图像并保存到流。 |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | 将形状渲染为 SVG 图像并保存到流。 |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | 初始化此类的新实例。 |
| static [Type](./type/)() |  |
## 另见

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
