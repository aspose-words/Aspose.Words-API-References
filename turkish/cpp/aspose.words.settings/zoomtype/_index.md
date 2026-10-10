---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::ZoomType enum. Microsoft Word'de C++ ile belgenin ekranda ne kadar büyük veya küçük görüneceğine ilişkin olası değerler."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Microsoft Word'de belgenin ekranda ne kadar büyük veya küçük göründüğüne ilişkin olası değerler.

```cpp
enum class ZoomType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Özel | 0 | Yakınlaştırma yüzdesi açıkça ayarlanmıştır. Kontrol boyutu değiştiğinde otomatik olarak yeniden hesaplanmaz. |
| None | n/a | Açık yakınlaştırma yüzdesinin kullanılacağını gösterir. Aynı [Custom](./) ile. |
| FullPage | 1 | Yakınlaştırma yüzdesi bir tam sayfaya sığacak şekilde otomatik olarak yeniden hesaplanır. |
| PageWidth | 2 | Yakınlaştırma yüzdesi sayfa genişliğine sığacak şekilde otom otomatik olarak yeniden hesaplanır. |
| TextFit | 3 | Yakınlaştırma yüzdesi metne sığacak şekilde otomatik olarak yeniden hesaplanır. |


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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
