---
title: "Aspose::Words::Document::get_LastSection yöntemi"
linktitle: "get_LastSection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_LastSection yöntemi. Belgedeki son bölümü C++'ta alır."
type: docs
weight: 35000
url: /tr/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


Belgedeki son bölümü alır.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## Örnekler



Bir belge oluşturucu ile yeni bir bölüm oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge varsayılan olarak bir bölüm içerir,
// ki içinde düzenleyebileceğimiz alt düğümler bulunur.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// İlk bölüme metin eklemek için bir belge oluşturucu kullanın.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Bir bölüm sonlandırması ekleyerek ikinci bir bölüm oluşturun.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Her bölümün kendi sayfa ayarları vardır.
// İkinci bölmedeki metni iki sütuna bölüştürebiliriz.
// Bu, ilk bölmedeki metni etkilemez.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## Ayrıca Bakınız

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
