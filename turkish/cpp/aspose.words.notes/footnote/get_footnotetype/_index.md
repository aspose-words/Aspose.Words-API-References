---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType method"
linktitle: "get_FootnoteType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType yöntemi. C++'da bunun bir dipnot mu yoksa sonnot mu olduğunu belirten bir değer döndürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


Bu nesnenin dipnot mu yoksa sonnot mu olduğunu belirten bir değer döndürür.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## Örnekler



Dipnotlar ile sonnotlar arasındaki farkı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda, metne numaralı referanslar eklemenin iki yolu verilmiştir. Bu referansların her ikisi de bir
// küçük üst simge referans işareti, onları eklediğimiz konuma.
// Referans işareti, varsayılan olarak, belgedeki tüm referanslar arasındaki referansın indeks numarasıdır.
// Her referans ayrıca bir giriş oluşturur; bu giriş, gövde metnindekiyle aynı referans işaretine sahip olacaktır
// ve referans metni, bunu belge oluşturucunun "InsertFootnote" yöntemine geçireceğiz.
// 1 -  Bir dipnot, girişinin referans verdiği metinle aynı sayfada görüneceği bir dipnot:
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  Belgenin sonunda görünecek bir dipnot, girişi:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## Ayrıca Bakınız

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
