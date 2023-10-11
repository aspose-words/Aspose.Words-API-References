---
title: InlineStory.IsDeleteRevision
second_title: Aspose.Words for .NET API Referansı
description: InlineStory mülk. Değişiklik izleme etkinken bu nesne Microsoft Wordde silinmişse true değerini döndürür.
type: docs
weight: 30
url: /tr/net/aspose.words/inlinestory/isdeleterevision/
---
## InlineStory.IsDeleteRevision property

Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true değerini döndürür.

```csharp
public bool IsDeleteRevision { get; }
```

### Örnekler

InlineStory düğümlerinin revizyonla ilgili özelliklerinin nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// Belgeyi düzenlediğimizde, Gözden Geçirme yoluyla bulunan "Değişiklikleri İzle" seçeneği -> Takip,
// Microsoft Word'de açıldığında uyguladığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyonları izlemeye şu şekilde başlayabiliriz:
// belgenin "StartTrackRevisions" yöntemini çağırıyoruz ve "StopTrackRevisions" yöntemini kullanarak izlemeyi durduruyoruz.
// Belgeye asimile etmek için düzeltmeleri kabul edebiliriz
// veya önerilen değişikliği geri almak ve atmak için bunları reddedin.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Aşağıda bir InlineStory düğümünü işaretleyebilecek beş tür revizyon bulunmaktadır.
// 1 - Bir "ekleme" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metin eklediğimizde meydana gelir.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - Bir "şuradan taşıma" revizyonu:
// Microsoft Word'de metni vurgulayıp belgede farklı bir yere sürüklediğimizde
// Değişiklikleri takip ederken iki revizyon belirir.
// "Şuradan taşı" revizyonu, metnin biz taşımadan önceki orijinal kopyasıdır.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - Bir "geçiş" revizyonu:
// "Taşı" revizyonu, belgedeki yeni konumuna taşıdığımız metindir.
// Gerçekleştirdiğimiz her hareket revizyonu için "Şuraya Taşı" ve "Şuraya Taşı" revizyonları çift olarak görünür.
// Bir taşıma revizyonunu kabul etmek, "şuradan taşıma" revizyonunu ve metnini siler,
// ve metni "şuraya taşı" revizyonundan korur.
// Bir taşıma revizyonunu reddetmek, tam tersine, "şuraya taşı" revizyonunu korur ve "şuraya taşı" revizyonunu siler.
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Bir "silme" revizyonu:
// Değişiklikleri takip ederken metni sildiğimizde bu revizyon meydana gelir. Bunun gibi bir metni sildiğimizde,
// biz revizyonu kabul edene kadar belgede revizyon olarak kalacak,
// bu, metni tamamen silecek veya revizyonu reddedecek, bu da sildiğimiz metni olduğu yerde tutacak.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Ayrıca bakınız

* class [InlineStory](../)
* ad alanı [Aspose.Words](../../inlinestory/)
* toplantı [Aspose.Words](../../../)


