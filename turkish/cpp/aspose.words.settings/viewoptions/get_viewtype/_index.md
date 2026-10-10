---
title: "Aspose::Words::Settings::ViewOptions::get_ViewType yöntemi"
linktitle: "get_ViewType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::ViewOptions::get_ViewType yöntemi. C++'ta Microsoft Word'deki görünüm modunu kontrol eder."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.settings/viewoptions/get_viewtype/
---
## ViewOptions::get_ViewType method


Microsoft Word'deki görünüm modunu kontrol eder.

```cpp
Aspose::Words::Settings::ViewType Aspose::Words::Settings::ViewOptions::get_ViewType() const
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

* Enum [ViewType](../../viewtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
