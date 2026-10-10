---
title: "Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints method"
linktitle: "get_BoundsInPoints"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints method. Şeklin gerçek sınırlarını nokta cinsinden C++'ta alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.rendering/noderendererbase/get_boundsinpoints/
---
## NodeRendererBase::get_BoundsInPoints method


Şeklin gerçek sınırlarını puan cinsinden alır.

```cpp
System::Drawing::RectangleF Aspose::Words::Rendering::NodeRendererBase::get_BoundsInPoints() const
```

## Açıklamalar


Bu özellik, şeklin gerçek (sayfada render edildiği gibi) sınırlayıcı kutusunu döndürür. Sınırlar, şekil dönüşünü (varsa) dikkate alır.

## Örnekler



Şekilleri ölçme ve ölçeklendirme yöntemlerini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));
auto renderer = System::MakeObject<Aspose::Words::Rendering::OfficeMathRenderer>(officeMath);

// OfficeMath nesnesinin render ettiğimizde oluşturacağı görüntünün boyutunu doğrulayın.
ASSERT_NEAR(122.0f, renderer->get_SizeInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_SizeInPoints().get_Height(), 0.15f);

ASSERT_NEAR(122.0f, renderer->get_BoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(13.0f, renderer->get_BoundsInPoints().get_Height(), 0.15f);

// Şeffaf bölümleri olan şekiller, "OpaqueBoundsInPoints" özelliklerinde farklı değerler içerebilir.
ASSERT_NEAR(119.5f, renderer->get_OpaqueBoundsInPoints().get_Width(), 0.25f);
ASSERT_NEAR(14.2f, renderer->get_OpaqueBoundsInPoints().get_Height(), 0.1f);

// Belirli bir DPI'ye lineer ölçekleme ile şeklin boyutunu piksellerde alın.
System::Drawing::Rectangle bounds = renderer->GetBoundsInPixels(1.0f, 96.0f);
System::String dpi96 = u"DPI 96";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96);
ASSERT_EQ(18, bounds.get_Height()) << (dpi96);

// Şeklin boyutunu piksellerde alın, ancak yatay ve dikey boyutlar için farklı DPI'ler kullanın.
bounds = renderer->GetBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150 = u"DPI 96 150";
ASSERT_EQ(163, bounds.get_Width()) << (dpi96150);
ASSERT_EQ(27, bounds.get_Height()) << (dpi96150);

// Opak sınırlar burada da değişebilir.
bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f);
System::String dpi96Opaque = u"DPI 96 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96Opaque);
ASSERT_EQ(19, bounds.get_Height()) << (dpi96Opaque);

bounds = renderer->GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
System::String dpi96150Opaque = u"DPI 96 150 Opaque";
ASSERT_EQ(160, bounds.get_Width()) << (dpi96150Opaque);
ASSERT_EQ(29, bounds.get_Height()) << (dpi96150Opaque);
```

## Ayrıca Bakınız

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
