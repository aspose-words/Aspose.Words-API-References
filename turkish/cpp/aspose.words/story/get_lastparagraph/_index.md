---
title: "Aspose::Words::Story::get_LastParagraph yöntemi"
linktitle: "get_LastParagraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Story::get_LastParagraph yöntemi. C++'da hikayedeki son paragrafı alır."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


Hikayedeki son paragrafı alır.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## Örnekler



[DocumentBuilder](../../documentbuilder/) nesnesinin imleç konumunu belirli bir düğüme nasıl taşıyacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// Belge oluşturucunun bir imleci vardır; bu imleç belgenin bir bölümü gibi davranır
// yapıcı, belge oluşturma yöntemlerini kullandığımızda yeni düğümler ekler.
// Bu imleç, Microsoft Word'ün yanıp sönen imleci gibi aynı şekilde çalışır,
// ve ayrıca, yapıcı tarafından yeni eklenen herhangi bir düğümün hemen sonuna da her zaman yerleşir.
// Belgenin farklı bir bölümüne içerik eklemek için,
// imleci "MoveTo" yöntemiyle başka bir düğüme taşıyabiliriz.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// İmleç artık taşındığı düğümün önündedir.
// İkinci bir run eklemek, onu ilk run'un önüne ekleyecektir.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// İmleci belgenin sonuna taşıyarak, daha önceki gibi metni sona eklemeye devam edebilirsiniz.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
