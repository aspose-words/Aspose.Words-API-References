---
title: "Aspose::Words::Rendering::NodeRendererBase::GetBoundsInPixels 方法"
linktitle: "GetBoundsInPixels"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::NodeRendererBase::GetBoundsInPixels 方法。计算形状在像素中的边界，针对指定的缩放因子和分辨率（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.rendering/noderendererbase/getboundsinpixels/
---
## NodeRendererBase::GetBoundsInPixels(float, float) method


根据指定的缩放因子和分辨率计算形状的像素边界。

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetBoundsInPixels(float scale, float dpi)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放因子（1.0 表示 100%）。 |
| dpi | float | 分辨率（水平和垂直），用于将点转换为像素（每英寸点数）。 |

### ReturnValue

形状在像素中的实际（页面渲染后的）边界框。
## 备注


此方法将 [BoundsInPoints](../get_boundsinpoints/) 转换为像素矩形。

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

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::GetBoundsInPixels(float, float, float) method


根据指定的缩放因子和分辨率计算形状的像素边界。

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放因子（1.0 表示 100%）。 |
| horizontalDpi | float | 水平分辨率，用于将点转换为像素（每英寸点数）。 |
| verticalDpi | float | 垂直分辨率，用于将点转换为像素（每英寸点数）。 |

### ReturnValue

形状在像素中的实际（页面渲染后的）边界框。
## 备注


此方法将 [BoundsInPoints](../get_boundsinpoints/) 转换为像素矩形。

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

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
