---
title: "Aspose::Words::Document::get_ViewOptions metodu"
linktitle: "get_ViewOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_ViewOptions yöntemi. Belge'nin Microsoft Word'de C++ içinde nasıl görüntüleneceğini kontrol etmek için seçenekler sağlar."
type: docs
weight: 58000
url: /tr/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


Belgenin Microsoft Word'de nasıl görüntüleneceğini kontrol etmek için seçenekler sağlar.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
```


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

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
