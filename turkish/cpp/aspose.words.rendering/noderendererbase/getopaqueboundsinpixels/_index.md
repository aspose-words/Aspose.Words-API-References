---
title: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels method"
linktitle: "GetOpaqueBoundsInPixels"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels yöntemi. Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin piksel cinsinden opak sınırlarını C++'da hesaplar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/
---
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float) method


Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını pikseller cinsinden hesaplar.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float dpi)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| scale | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| dpi | float | Noktalardan piksellere dönüştürmek için çözünürlük (inç başına nokta). |

### ReturnValue

Şeklin piksel cinsinden opak dikdörtgeni.
## Açıklamalar


Bu yöntem, [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) öğesini piksel cinsinden dikdörtgene dönüştürür ve şeklin yalnızca opak kısmıyla render etmek için bir bitmap oluşturmak istediğinizde faydalıdır.

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
## NodeRendererBase::GetOpaqueBoundsInPixels(float, float, float) method


Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını pikseller cinsinden hesaplar.

```cpp
System::Drawing::Rectangle Aspose::Words::Rendering::NodeRendererBase::GetOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| scale | float | Yakınlaştırma faktörü (1.0, %100'e eşittir). |
| horizontalDpi | float | Noktalardan piksellere dönüştürmek için yatay çözünürlük (inç başına nokta). |
| verticalDpi | float | Noktalardan piksellere dönüştürmek için dikey çözünürlük (inç başına nokta). |

### ReturnValue

Şeklin piksel cinsinden opak dikdörtgeni.
## Açıklamalar


Bu yöntem, [OpaqueBoundsInPoints](../get_opaqueboundsinpoints/) öğesini piksel cinsinden dikdörtgene dönüştürür ve şeklin yalnızca opak kısmıyla render etmek için bir bitmap oluşturmak istediğinizde faydalıdır.

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
