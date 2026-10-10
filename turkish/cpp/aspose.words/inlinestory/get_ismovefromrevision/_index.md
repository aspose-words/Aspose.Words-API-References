---
title: "Aspose::Words::InlineStory::get_IsMoveFromRevision metodu"
linktitle: "get_IsMoveFromRevision"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::InlineStory::get_IsMoveFromRevision metodu. C++'ta değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse) true döndürür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/inlinestory/get_ismovefromrevision/
---
## InlineStory::get_IsMoveFromRevision method


Bu nesne, değişiklik izleme etkinken Microsoft Word'de taşınmış (silinmiş) ise **true** döndürür.

```cpp
bool Aspose::Words::InlineStory::get_IsMoveFromRevision()
```


## Örnekler



[InlineStory](../) düğümlerinin revizyonla ilgili özelliklerini nasıl görüntüleyeceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision footnotes.docx");

// Belgeyi, Review -> Tracking üzerinden bulunan "Track Changes" seçeneği açıkken düzenlediğimizde,
// Microsoft Word'de etkinleştirildiğinde, yaptığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyon izlemeye şu şekilde başlayabiliriz
// "StartTrackRevisions" yöntemini belge üzerinde çağırarak ve "StopTrackRevisions" yöntemini kullanarak izlemeyi durdurabilirsiniz.
// Revizyonları kabul ederek belgeye dahil edebiliriz
// veya önerilen değişikliği geri almak ve iptal etmek için reddedin.
ASSERT_TRUE(doc->get_HasRevisions());

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Notes::Footnote>>> footnotes = doc->GetChildNodes(Aspose::Words::NodeType::Footnote, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Notes::Footnote> >()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// Aşağıda bir InlineStory düğümünü işaretleyebilen beş revizyon türü bulunmaktadır.
// 1 -  Bir "insert" revizyonu:
// Bu revizyon, değişiklikleri izlerken metin eklediğimizde ortaya çıkar.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  \"move from\" revizyonu:
// Microsoft Word'de metni vurguladığımızda ve ardından belge içinde farklı bir yere sürüklediğimizde
// değişiklikleri izlerken iki revizyon ortaya çıkar.
// "move from" revizyonu, metni taşımadan önceki orijinal kopyasıdır.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  \"move to\" revizyonu:
// "move to" revizyonu, belge içinde yeni konumunda taşıdığımız metindir.
// "Move from" ve "move to" revizyonları, gerçekleştirdiğimiz her taşıma revizyonu için çiftler halinde görünür.
// Bir taşıma revizyonunu kabul etmek, "move from" revizyonunu ve metnini siler,
// ve "move to" revizyonundaki metni tutar.
// Bir taşıma revizyonunu reddetmek ise "move from" revizyonunu tutar ve "move to" revizyonunu siler.
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  \"delete\" revizyonu:
// Bu revizyon, değişiklikleri izlerken metni sildiğimizde ortaya çıkar. Böyle bir metni sildiğimizde,
// metin, revizyonu kabul edene kadar belge içinde bir revizyon olarak kalır,
// bu, metni kalıcı olarak siler; ya da revizyonu reddeder, bu da sildiğimiz metni olduğu yerde tutar.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## Ayrıca Bakınız

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
