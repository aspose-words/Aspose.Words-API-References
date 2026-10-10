---
title: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage metodu"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage metodu. AppendDocument() çağrıldığında ilk içe aktarılan bölüm tipini NewPage olarak zorla değiştireceğini belirten bir boolean değeri alır veya ayarlar. Varsayılan değer C++'da true'dir."
type: docs
weight: 3500
url: /tr/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


İlk içe aktarılan bölüm tipini [NewPage](../../sectionstart/) olarak zorla değiştireceğini belirten bir boolean değeri alır veya ayarlar. [AppendDocument()](../) çağrıldığında. Varsayılan değer **true**'dır.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## Örnekler



Orijinal bölüm tipinin nasıl korunacağını gösterir.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
