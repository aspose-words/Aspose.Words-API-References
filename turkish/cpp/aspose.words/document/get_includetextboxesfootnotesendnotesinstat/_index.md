---
title: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat yöntemi"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat yöntemi. C++'da kelime sayımı istatistiklerine metin kutularını, dipnotları ve son notları dahil edip etmeyeceğini belirtir."
type: docs
weight: 33000
url: /tr/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


Kelime sayımı istatistiklerine metin kutularını, dipnotları ve son notları dahil edilip edilmeyeceğini belirtir.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## Örnekler



Metin kutularını, dipnotları ve son notları kelime sayımı istatistiklerine dahil etme veya hariç tutma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// Varsayılan olarak seçenek 'false' olarak ayarlanmıştır.
doc->UpdateWordCount();
// Metin kutuları, dipnotlar ve son notlar olmadan kelime sayısı.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// Metin kutuları, dipnotlar ve son notlar dahil kelime sayısı.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
