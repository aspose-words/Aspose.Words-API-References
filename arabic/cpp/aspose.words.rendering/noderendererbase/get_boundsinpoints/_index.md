---
title: "Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints method"
linktitle: "get_BoundsInPoints"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints. يحصل على الحدود الفعلية للشكل بالنقاط في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.rendering/noderendererbase/get_boundsinpoints/
---
## NodeRendererBase::get_BoundsInPoints method


يحصل على الحدود الفعلية للشكل بالنقاط.

```cpp
System::Drawing::RectangleF Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints() const
```

## ملاحظات


هذه الخاصية تُعيد الصندوق المحيط الفعلي (كما يُعرض على الصفحة) للشكل. تأخذ الحدود في الاعتبار دوران الشكل (إن وجد).

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
