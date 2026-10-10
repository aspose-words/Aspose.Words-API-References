---
title: "Aspose::Words::Settings::ViewOptions sınıfı"
linktitle: "ViewOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::ViewOptions sınıfı. Bir belgenin Microsoft Word'de nasıl gösterileceğini kontrol eden çeşitli seçenekler sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


Bir belgenin Microsoft Word'de nasıl gösterileceğini kontrol eden çeşitli seçenekler sağlar. Daha fazla bilgi için, [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/) dokümantasyon makalesini ziyaret edin.

```cpp
class ViewOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | Yazdırma düzeni görünümünde arka plan şeklinin görüntülenmesini kontrol eder. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır. |
| [get_FormsDesign](./get_formsdesign/)() const | Belgenin form tasarım modunda olup olmadığını belirtir. |
| [get_ViewType](./get_viewtype/)() const | Microsoft Word'deki görünüm modunu kontrol eder. |
| [get_ZoomPercent](./get_zoompercent/)() const | Belgenizi görmek istediğiniz yüzdeyi alır veya ayarlar. |
| [get_ZoomType](./get_zoomtype/)() const | Pencere boyutuna göre bir yakınlaştırma değeri alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | Ayarlayıcı: [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/). |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | Ayarlayıcı: [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/). |
| [set_FormsDesign](./set_formsdesign/)(bool) | Ayarlayıcı: [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/). |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | Ayarlayıcı: [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/). |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | Ayarlayıcı: [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/). |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | Ayarlayıcı: [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/). |
| static [Type](./type/)() |  |

## Örnekler



Microsoft Word'ün eski sürümlerinin bir belge yüklendiğinde uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


Özel bir yakınlaştırma türünün nasıl ayarlanacağını gösterir; Microsoft Word'ün eski sürümleri belge yüklendiğinde bunu uygular.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Microsoft Word'ü elde etmek için "ZoomType" özelliğini "ZoomType.PageWidth" olarak ayarlayın
// belgeyi otomatik olarak sayfanın genişliğine sığdıracak şekilde yakınlaştırmak için.
// Microsoft Word'ü elde etmek için "ZoomType" özelliğini "ZoomType.FullPage" olarak ayarlayın
// belgeyi otomatik olarak tüm ilk sayfayı görünür kılacak şekilde yakınlaştırmak için.
// Microsoft Word'ü elde etmek için "ZoomType" özelliğini "ZoomType.TextFit" olarak ayarlayın
// belgeyi otomatik olarak ilk sayfanın iç metin kenar boşluklarına sığdıracak şekilde yakınlaştırmak için.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
