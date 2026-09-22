---
title: "Aspose::Words::Paragraph::get_IsMoveFromRevision metodu"
linktitle: "get_IsMoveFromRevision"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::get_IsMoveFromRevision metodu. C++'ta değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse) true döndürür."
type: docs
weight: 16000
url: /tr/cpp/aspose.words/paragraph/get_ismovefromrevision/
---
## Paragraph::get_IsMoveFromRevision method


Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür.

```cpp
bool Aspose::Words::Paragraph::get_IsMoveFromRevision()
```


## Örnekler



Bir paragrafın taşıma revizyonu olup olmadığını nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Bu belge, imleçle metni vurguladığımızda ortaya çıkan "Move" revizyonlarını içerir,
// ve ardından başka bir konuma taşımak için sürüklediğimizde
// Microsoft Word'de "Review" -> "Track changes" yoluyla revizyonları izlerken.
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// "Move from" ve "Move to" revizyon çiftlerinden oluşur.
// Bu revizyonlar, belgeye yapılabilecek ve kabul edebileceğimiz ya da reddedebileceğimiz potansiyel değişikliklerdir.
// Bir taşıma revizyonunu kabul etmeden/reddetmeden önce, belge
// metnin hem çıkış hem de varış konumlarını izlemek zorundadır.
// İkinci ve dördüncü paragraf, bu tür bir revizyonu tanımlar ve bu nedenle ikisi de aynı içeriğe sahiptir.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// "Move from" revizyonu, metni sürüklediğimiz paragraftır.
// Revizyonu kabul edersek, bu paragraf kaybolur,
// ve diğer paragraf kalır ve artık bir revizyon olmaz.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// "Move to" revizyonu, metni sürüklediğimiz paragraftır.
// Revizyonu reddederseniz, bu paragraf kaybolur ve diğer paragraf kalır.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## Ayrıca Bakınız

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
