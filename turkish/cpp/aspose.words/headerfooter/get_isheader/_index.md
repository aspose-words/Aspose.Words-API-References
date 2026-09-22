---
title: "Aspose::Words::HeaderFooter::get_IsHeader yöntemi"
linktitle: "get_IsHeader"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::HeaderFooter::get_IsHeader yöntemi. Bu HeaderFooter nesnesi C++'ta bir başlık ise Doğru."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/headerfooter/get_isheader/
---
## HeaderFooter::get_IsHeader method


Bu [HeaderFooter](../) nesnesi bir başlık ise Doğru.

```cpp
bool Aspose::Words::HeaderFooter::get_IsHeader()
```


## Örnekler



Bir üstbilgi ve altbilgi oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir üstbilgi oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının üst kısmında, ana metnin üzerinde görünecek.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Bir altbilgi oluşturun ve ona bir paragraf ekleyin. O paragraftaki metin
// bu bölümün her sayfasının alt kısmında, ana metnin altında görünecek.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## Ayrıca Bakınız

* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
