---
title: "Aspose::Words::Rendering::NodeRendererBase::get_OpaqueBoundsInPoints method"
linktitle: "get_OpaqueBoundsInPoints"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Rendering::NodeRendererBase::get_OpaqueBoundsInPoints. يحصل على الحدود غير الشفافة للشكل بالنقاط في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.rendering/noderendererbase/get_opaqueboundsinpoints/
---
## NodeRendererBase::get_OpaqueBoundsInPoints method


يحصل على الحدود غير الشفافة للشكل بالنقاط.

```cpp
System::Drawing::RectangleF Aspose::Words::Rendering::NodeRendererBase::get_OpaqueBoundsInPoints()
```

## ملاحظات


هذه الخاصية تُعيد الصندوق المحيط غير الشفاف (أي يتم تجاهل الأجزاء الشفافة من الشكل) للشكل. تأخذ الحدود دوران الشكل في الاعتبار.

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

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
