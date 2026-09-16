---
title: "Aspose::Words::Rendering::OfficeMathRenderer class"
linktitle: "OfficeMathRenderer"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::OfficeMathRenderer 类。提供将单个 OfficeMath 渲染为光栅或矢量图像或渲染到 Graphics 对象的方法。欲了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class


提供将单个 [OfficeMath](../../aspose.words.math/officemath/) 渲染为光栅或矢量图像并渲染到 Graphics 对象的方法。欲了解更多，请访问 [Working with OfficeMath](https://docs.aspose.com/words/cpp/working-with-officemath/) 文档文章。

```cpp
class OfficeMathRenderer : public Aspose::Words::Rendering::NodeRendererBase
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
| [OfficeMathRenderer](./officemathrenderer/)(const System::SharedPtr\<Aspose::Words::Math::OfficeMath\>\&) | 初始化此类的新实例。 |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | 将形状渲染到 **Graphics** 对象，使用指定的比例。 |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | 将形状渲染到 **Graphics** 对象，使用指定的大小。 |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | 将形状渲染为图像并保存到文件。 |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | 将形状渲染为 SVG 图像并保存到文件。 |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | 将形状渲染为图像并保存到流。 |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | 将形状渲染为 SVG 图像并保存到流。 |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
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

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
