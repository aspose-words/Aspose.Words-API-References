---
title: "Aspose::Words::ParagraphCollection sınıfı"
linktitle: "ParagraphCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphCollection sınıfı. Paragraph düğümlerinin bir koleksiyonuna tip güvenli erişim sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 48000
url: /tr/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


Paragraph düğümlerinin bir koleksiyonuna tip güvenli erişim sağlar. Daha fazla bilgi edinmek için [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) dokümantasyon makalesini ziyaret edin.

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümü koleksiyonun sonuna ekler. |
| [Clear](../nodecollection/clear/)() | Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [get_Count](../nodecollection/get_count/)() | Koleksiyondaki düğüm sayısını alır. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Verilen indeksdeki bir [Paragraph](../paragraph/) öğesini alır. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen düğümün sıfır tabanlı indeksini döndürür. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen indeksde bir düğümü koleksiyona ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Belirtilen indeksteki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](./toarray/)() | Koleksiyondaki tüm paragrafları yeni bir paragraf dizisine kopyalar. |
| static [Type](./type/)() |  |

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

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
