---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method"
linktitle: "get_ZoomPercent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method. C++'da belgenizi görmek istediğiniz yüzdeyi alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


Belgenizi görmek istediğiniz yüzdeyi alır veya ayarlar.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
```

## Açıklamalar


Aspose.Words bu seçeneği okuyup yazabilse de, kullanımı uygulamaya özgüdür. Örneğin MS Word 2013 bu seçeneğin değerine saygı göstermez.

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

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
