---
title: "Aspose::Words::DocumentBuilder::get_Document yöntemi"
linktitle: "get_Document"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::get_Document yöntemi. Bu nesnenin bağlı olduğu Document nesnesini alır veya ayarlar C++'ta."
type: docs
weight: 16000
url: /tr/cpp/aspose.words/documentbuilder/get_document/
---
## DocumentBuilder::get_Document method


Bu nesnenin bağlı olduğu [Document](./) nesnesini alır veya ayarlar.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::DocumentBuilder::get_Document() const
```


## Örnekler



Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Oluşturucunun geçerli bölümü için sayfa ayarı özelliklerini değiştirin ve metin ekleyin.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Bir belge oluşturucu kullanarak yeni bir bölüm başlatırsak,
// oluşturucunun geçerli sayfa ayarı özelliklerini devralacaktır.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Sayfa ayarı özelliklerini varsayılan değerlerine geri döndürmek için "ClearFormatting" yöntemini kullanabiliriz.
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Ayrıca Bakınız

* Class [Document](../../document/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
