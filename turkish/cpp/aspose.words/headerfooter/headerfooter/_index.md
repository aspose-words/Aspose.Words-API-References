---
title: "Aspose::Words::HeaderFooter::HeaderFooter yapıcı"
linktitle: "HeaderFooter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::HeaderFooter::HeaderFooter yapıcı. Belirtilen tipte yeni bir başlık veya altbilgi C++'ta oluşturur."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter::HeaderFooter constructor


Belirtilen tipte yeni bir üstbilgi veya altbilgi oluşturur.

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
| headerFooterType | Aspose::Words::HeaderFooterType | Başlık veya altbilginin tipini belirten bir [HeaderFooterType](../get_headerfootertype/) değeri. |
## Açıklamalar


[HeaderFooter](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve [ParentNode](../../node/get_parentnode/) **null** değerindedir.

Bir [HeaderFooter](../) öğesini bir [Section](../../section/) öğesine eklemek için [InsertAfter1()</see>, <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) kullanın veya [HeadersFooters](../../section/get_headersfooters/) özelliğini ve [Add()](../), [Insert()](../) yöntemlerini kullanın.

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

* Class [DocumentBase](../../documentbase/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
