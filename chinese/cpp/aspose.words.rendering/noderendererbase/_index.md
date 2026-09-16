---
title: "Aspose::Words::Rendering::NodeRendererBase 类"
linktitle: "NodeRendererBase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::NodeRendererBase 类。ShapeRenderer 和 OfficeMathRenderer 的基类。了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class


用于 [ShapeRenderer](../shaperenderer/) 和 [OfficeMathRenderer](../officemathrenderer/) 的基类。了解更多，请访问 [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) 文档文章。

```cpp
class NodeRendererBase : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BoundsInPoints](./get_boundsinpoints/)() const | 获取形状的实际边界（以点为单位）。 |
| [get_OpaqueBoundsInPoints](./get_opaqueboundsinpoints/)() | 获取形状的不透明边界（以点为单位）。 |
| [get_SizeInPoints](./get_sizeinpoints/)() | 获取形状的实际大小（以点为单位）。 |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float) | 根据指定的缩放因子和分辨率计算形状的像素边界。 |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float, float) | 根据指定的缩放因子和分辨率计算形状的像素边界。 |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float) | 根据指定的缩放因子和分辨率计算形状的不透明像素边界。 |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float, float) | 根据指定的缩放因子和分辨率计算形状的不透明像素边界。 |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | 根据指定的缩放因子和分辨率计算形状的像素大小。 |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | 根据指定的缩放因子和分辨率计算形状的像素大小。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](./noderendererbase/)() |  |
| [RenderToScale](./rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | 将形状渲染到 **Graphics** 对象，使用指定的比例。 |
| [RenderToSize](./rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | 将形状渲染到 **Graphics** 对象，使用指定的大小。 |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | 将形状渲染为图像并保存到文件。 |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | 将形状渲染为 SVG 图像并保存到文件。 |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | 将形状渲染为图像并保存到流。 |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | 将形状渲染为 SVG 图像并保存到流。 |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

## 示例



展示如何测量和缩放形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// 验证在渲染时 OfficeMath 对象将创建的图像大小。
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties。
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// 获取形状的像素尺寸，使用线性缩放到特定 DPI。
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// 获取形状的像素尺寸，但水平和垂直维度使用不同的 DPI。
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// 不透明边界在此也可能有所变化。
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## 另见

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
