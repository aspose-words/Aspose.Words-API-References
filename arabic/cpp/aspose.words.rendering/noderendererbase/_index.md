---
title: "Aspose::Words::Rendering::NodeRendererBase فئة"
linktitle: "NodeRendererBase"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Rendering::NodeRendererBase فئة. الفئة الأساسية لـ ShapeRenderer و OfficeMathRenderer. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class


الفئة الأساسية لـ [ShapeRenderer](../shaperenderer/) و [OfficeMathRenderer](../officemathrenderer/). لمعرفة المزيد، زر مقالة الوثائق [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class NodeRendererBase : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BoundsInPoints](./get_boundsinpoints/)() const | يحصل على الحدود الفعلية للشكل بالنقاط. |
| [get_OpaqueBoundsInPoints](./get_opaqueboundsinpoints/)() | يحصل على الحدود غير الشفافة للشكل بالنقاط. |
| [get_SizeInPoints](./get_sizeinpoints/)() | يحصل على الحجم الفعلي للشكل بالنقاط. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float, float) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float) | يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float, float) | يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](./noderendererbase/)() |  |
| [RenderToScale](./rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | يرسم الشكل داخل كائن **Graphics** إلى مقياس محدد. |
| [RenderToSize](./rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | يرسم الشكل داخل كائن **Graphics** إلى حجم محدد. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | يرسم الشكل إلى صورة ويحفظها في ملف. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | يرسم الشكل إلى صورة SVG ويحفظها في ملف. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | يرسم الشكل إلى صورة ويحفظها في تدفق. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | يرسم الشكل إلى صورة SVG ويحفظها في تدفق. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية قياس وتكبير الأشكال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// تحقق من حجم الصورة التي سينشئها كائن OfficeMath عند رسمه.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// قد تحتوي الأشكال ذات الأجزاء الشفافة على قيم مختلفة في خاصية "OpaqueBoundsInPoints".
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// احصل على حجم الشكل بالبكسل، مع تكبير خطي إلى DPI محدد.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// احصل على حجم الشكل بالبكسل، لكن مع DPI مختلف للأبعاد الأفقية والرأسية.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// قد تختلف الحدود غير الشفافة هنا أيضًا.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## انظر أيضًا

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
