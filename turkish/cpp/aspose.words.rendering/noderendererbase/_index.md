---
title: "Aspose::Words::Rendering::NodeRendererBase class"
linktitle: "NodeRendererBase"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::NodeRendererBase class. ShapeRenderer ve OfficeMathRenderer için temel sınıf. Daha fazla bilgi için C++'deki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class


Base class for [ShapeRenderer](../shaperenderer/) and [OfficeMathRenderer](../officemathrenderer/). Daha fazla bilgi için [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) dokümantasyon makalesini ziyaret edin.

```cpp
class NodeRendererBase : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BoundsInPoints](./get_boundsinpoints/)() const | Şeklin gerçek sınırlarını puan cinsinden alır. |
| [get_OpaqueBoundsInPoints](./get_opaqueboundsinpoints/)() | Şeklin opak sınırlarını puan cinsinden alır. |
| [get_SizeInPoints](./get_sizeinpoints/)() | Şeklin gerçek boyutunu puan cinsinden alır. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını pikseller cinsinden hesaplar. |
| [GetBoundsInPixels](./getboundsinpixels/)(float, float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını pikseller cinsinden hesaplar. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını pikseller cinsinden hesaplar. |
| [GetOpaqueBoundsInPixels](./getopaqueboundsinpixels/)(float, float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını pikseller cinsinden hesaplar. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu pikseller cinsinden hesaplar. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu pikseller cinsinden hesaplar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](./noderendererbase/)() |  |
| [RenderToScale](./rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Şekli belirtilen ölçeğe **Graphics** nesnesine çizer. |
| [RenderToSize](./rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Şekli belirtilen boyuta **Graphics** nesnesine çizer. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Şekli bir görüntüye render eder ve bir dosyaya kaydeder. |
| [Save](./save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Şekli bir SVG görüntüsüne render eder ve bir dosyaya kaydeder. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Şekli bir görüntüye render eder ve bir akışa kaydeder. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Şekli bir SVG görüntüsüne render eder ve bir akışa kaydeder. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
