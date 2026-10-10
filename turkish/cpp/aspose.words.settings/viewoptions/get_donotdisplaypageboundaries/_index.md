---
title: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries metodu"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries metodu. C++'ta metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## Örnekler



Görünüm seçeneklerinde dikey boşlukları ve üstbilgi/altbilgileri nasıl gizleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 3 sayfa boyunca uzanan içerik ekleyin.
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// Bir üstbilgi ve bir altbilgi ekleyin.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// Bu belge, birkaç tam sayfa kadar alan kaplayan az miktarda içerik içerir.
// Microsoft Word'ün eski sürümlerinin üstbilgileri atlamasını sağlamak için "DoNotDisplayPageBoundaries" bayrağını "true" olarak ayarlayın,
// altbilgileri ve belgeyi görüntülerken çok sayıda dikey boşluğu da atlamasını sağlar.
// Microsoft Word'ün eski sürümlerinin belgeyi normal şekilde görüntülemesi için "DoNotDisplayPageBoundaries" bayrağını "false" olarak ayarlayın
// belgemizi normal olarak görüntülemek için.
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## Ayrıca Bakınız

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
