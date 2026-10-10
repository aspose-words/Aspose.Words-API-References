---
title: "Aspose::Words::Inline::get_IsDeleteRevision yöntemi"
linktitle: "get_IsDeleteRevision"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Inline::get_IsDeleteRevision yöntemi. Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true döndürür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/inline/get_isdeleterevision/
---
## Inline::get_IsDeleteRevision method


Bu nesne, değişiklik izleme etkinken Microsoft Word'de silinmişse true döndürür.

```cpp
bool Aspose::Words::Inline::get_IsDeleteRevision()
```


## Örnekler



Satır içi bir düğümün revizyon tipinin nasıl belirleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Belgeyi, Review -> Tracking üzerinden bulunan "Track Changes" seçeneği açıkken düzenlediğimizde,
// Microsoft Word'de etkinleştirildiğinde, yaptığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyon izlemeye şu şekilde başlayabiliriz
// "StartTrackRevisions" yöntemini belge üzerinde çağırarak ve "StopTrackRevisions" yöntemini kullanarak izlemeyi durdurabilirsiniz.
// Revizyonları kabul ederek belgeye dahil edebiliriz
// veya reddederek önerilen değişikliği etkili bir şekilde iptal edebiliriz.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Bir revizyonun üst düğümü, revizyonun ilgili olduğu Run'dur. Run, bir Inline düğümdür.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Aşağıda bir Inline düğümünü işaretleyebilen beş revizyon türü bulunmaktadır.
// 1 -  Bir "insert" revizyonu:
// Bu revizyon, değişiklikleri izlerken metin eklediğimizde ortaya çıkar.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Bir "format" revizyonu:
// Bu revizyon, değişiklikleri izlerken metnin biçimlendirmesini değiştirdiğimizde ortaya çıkar.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Bir "move from" revizyonu:
// Microsoft Word'de metni vurguladığımızda ve ardından belge içinde farklı bir yere sürüklediğimizde
// değişiklikleri izlerken iki revizyon ortaya çıkar.
// "move from" revizyonu, metni taşımadan önceki orijinal kopyasıdır.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Bir "move to" revizyonu:
// "move to" revizyonu, belge içinde yeni konumunda taşıdığımız metindir.
// "Move from" ve "move to" revizyonları, gerçekleştirdiğimiz her taşıma revizyonu için çiftler halinde görünür.
// Bir taşıma revizyonunu kabul etmek, "move from" revizyonunu ve metnini siler,
// ve "move to" revizyonundaki metni tutar.
// Bir taşıma revizyonunu reddetmek ise "move from" revizyonunu tutar ve "move to" revizyonunu siler.
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Bir "delete" revizyonu:
// Bu revizyon, değişiklikleri izlerken metni sildiğimizde ortaya çıkar. Böyle bir metni sildiğimizde,
// metin, revizyonu kabul edene kadar belge içinde bir revizyon olarak kalır,
// bu, metni kalıcı olarak siler; ya da revizyonu reddeder, bu da sildiğimiz metni olduğu yerde tutar.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Ayrıca Bakınız

* Class [Inline](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
