---
title: "فئة Aspose::Words::Rendering::OfficeMathRenderer"
linktitle: "OfficeMathRenderer"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Rendering::OfficeMathRenderer. توفر طرقًا لتصوير OfficeMath فردي إلى صورة نقطية أو متجهة أو إلى كائن Graphics. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class


توفر طرقًا لتصوير [OfficeMath](../../aspose.words.math/officemath/) فردي إلى صورة نقطية أو متجهة أو إلى كائن Graphics. لمعرفة المزيد، زر مقالة الوثائق [Working with OfficeMath](https://docs.aspose.com/words/cpp/working-with-officemath/).

```cpp
class OfficeMathRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | يحصل على الحدود الفعلية للشكل بالنقاط. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | يحصل على الحدود غير الشفافة للشكل بالنقاط. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | يحصل على الحجم الفعلي للشكل بالنقاط. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | يحسب حدود الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | يحسب الحدود غير الشفافة للشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | يحسب حجم الشكل بالبكسل لعامل تكبير ودقة محددين. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [OfficeMathRenderer](./officemathrenderer/)(const System::SharedPtr\<Aspose::Words::Math::OfficeMath\>\&) | يُنشئ مثيلًا جديدًا لهذه الفئة. |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | يرسم الشكل داخل كائن **Graphics** إلى مقياس محدد. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | يرسم الشكل داخل كائن **Graphics** إلى حجم محدد. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | يرسم الشكل إلى صورة ويحفظها في ملف. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | يرسم الشكل إلى صورة SVG ويحفظها في ملف. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | يرسم الشكل إلى صورة ويحفظها في تدفق. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | يرسم الشكل إلى صورة SVG ويحفظها في تدفق. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
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

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
