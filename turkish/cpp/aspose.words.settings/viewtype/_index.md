---
title: "Aspose::Words::Settings::ViewType enum"
linktitle: "ViewType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::ViewType enum. Microsoft Word'de C++ için görünüm modunun olası değerleri."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Microsoft Word'de görünüm modu için olası değerler.

```cpp
enum class ViewType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Belge, uygulamanın varsayılan görünümünde görüntülenecektir. |
| Reading | 0 | Belge, uygulamanın varsayılan görünümünde görüntülenecektir. |
| PageLayout | 1 | Belge, belgenin nasıl yazdırılacağını gösteren bir görünümde açılacaktır. |
| Outline | 3 | Belge, taslak oluşturma veya uzun belgeler oluşturma için optimize edilmiş bir görünümde görüntülenecektir. |
| Normal | 4 | Belge, taslak oluşturma veya uzun belgeler oluşturma için optimize edilmiş bir görünümde görüntülenecektir. |
| Web | 5 | Belge, bu belgenin bir web sayfasında nasıl görüntüleneceğini taklit eden bir görünümde görüntülenecektir. |


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
