---
title: InlineStory.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: .NET için Aspose.Words
description: InlineStory'nin IsMoveFromRevision özelliğini keşfedin. Sorunsuz düzenleme için değişiklik izlemeyi etkinleştirerek Microsoft Word'de taşınan veya silinen içeriği kolayca izleyin.
type: docs
weight: 50
url: /tr/net/aspose.words/inlinestory/ismovefromrevision/
---
## InlineStory.IsMoveFromRevision property

Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse).

```csharp
public bool IsMoveFromRevision { get; }
```

## Örnekler

InlineStory düğümlerinin revizyonla ilgili özelliklerinin nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// İnceleme -> İzleme'de bulunan "Değişiklikleri İzle" seçeneğiyle belgeyi düzenlediğimizde,
// Microsoft Word'de açık olduğunda uyguladığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyonları şu şekilde izlemeye başlayabiliriz:
// belgenin "StartTrackRevisions" metodunu çağırarak ve "StopTrackRevisions" metodunu kullanarak izlemeyi durdurarak.
// Revizyonları belgeye entegre etmek için kabul edebiliriz
// veya önerilen değişikliği geri almak ve atmak için bunları reddedin.
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// Aşağıda, bir InlineStory düğümünü işaretleyebilecek beş tür revizyon bulunmaktadır.
// 1 - Bir "ekle" revizyon:
// Bu revizyon, değişiklikleri izlerken metin eklediğimizde gerçekleşir.
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - "Taşınma" revizyonundan:
// Microsoft Word'de metni vurguladığımızda ve ardından onu belgede farklı bir yere sürüklediğimizde
// Değişiklikleri izlerken iki revizyon görünüyor.
// "Taşıma" revizyonunun kopyası, taşımadan önce metnin orijinal halinin bir kopyasıdır.
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 - "Taşınacak" revizyon:
// "Taşı" revizyon, belgedeki yeni konumuna taşıdığımız metindir.
// Gerçekleştirdiğimiz her taşıma revizyonu için "Şuradan taşı" ve "Şuraya taşı" revizyonları çiftler halinde görünür.
// Bir taşıma revizyonunu kabul etmek, "taşınacak" revizyonunu ve metnini siler,
// ve "taşınacak" revizyondaki metni tutar.
// Bir taşıma revizyonunu reddetmek ise tam tersine "taşınacak yer" revizyonunu korur ve "taşınacak yer" revizyonunu siler.
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - Bir "silme" revizyonu:
// Bu revizyon, değişiklikleri izlerken metni sildiğimizde meydana gelir. Metni bu şekilde sildiğimizde,
// revizyonu kabul edene kadar belgede bir revizyon olarak kalacaktır,
// ya metni tamamen silecek ya da revizyonu reddedecek, bu da sildiğimiz metni olduğu yerde tutacak.
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### Ayrıca bakınız

* class [InlineStory](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
