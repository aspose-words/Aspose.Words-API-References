---
title: Inline.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: .NET için Aspose.Words
description: Microsoft Word'deki Inline IsMoveFromRevision özelliğini keşfedin. Etkili belge yönetimi ve düzenlemesi için silinen nesneleri nasıl izlediğini öğrenin.
type: docs
weight: 50
url: /tr/net/aspose.words/inline/ismovefromrevision/
---
## Inline.IsMoveFromRevision property

Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (silinirse).

```csharp
public bool IsMoveFromRevision { get; }
```

## Örnekler

Satır içi bir düğümün revizyon türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// İnceleme -> İzleme'de bulunan "Değişiklikleri İzle" seçeneğiyle belgeyi düzenlediğimizde,
// Microsoft Word'de açık olduğunda uyguladığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyonları şu şekilde izlemeye başlayabiliriz:
// belgenin "StartTrackRevisions" metodunu çağırarak ve "StopTrackRevisions" metodunu kullanarak izlemeyi durdurarak.
// Revizyonları belgeye entegre etmek için kabul edebiliriz
// veya önerilen değişikliği etkili bir şekilde değiştirmek için bunları reddedin.
Assert.AreEqual(6, doc.Revisions.Count);

// Bir revizyonun üst düğümü, revizyonun ilgilendiği çalıştırmadır. Bir Çalıştırma, bir Satır İçi düğümdür.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Aşağıda, bir Inline düğümünü işaretleyebilecek beş tür revizyon bulunmaktadır.
// 1 - Bir "ekle" revizyon:
// Bu revizyon, değişiklikleri izlerken metin eklediğimizde gerçekleşir.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Bir "format" revizyonu:
// Bu revizyon, değişiklikleri izlerken metnin biçimlendirmesini değiştirdiğimizde gerçekleşir.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - "Taşınma" revizyonundan:
// Microsoft Word'de metni vurguladığımızda ve ardından onu belgede farklı bir yere sürüklediğimizde
// Değişiklikleri izlerken iki revizyon görünüyor.
// "Taşıma" revizyonunun kopyası, taşımadan önce metnin orijinal halinin bir kopyasıdır.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - "Taşınacak" revizyon:
// "Taşı" revizyon, belgedeki yeni konumuna taşıdığımız metindir.
// Gerçekleştirdiğimiz her taşıma revizyonu için "Şuradan taşı" ve "Şuraya taşı" revizyonları çiftler halinde görünür.
// Bir taşıma revizyonunu kabul etmek, "taşınacak" revizyonunu ve metnini siler,
// ve "taşınacak" revizyondaki metni tutar.
// Bir taşıma revizyonunu reddetmek ise tam tersine "taşınacak yer" revizyonunu korur ve "taşınacak yer" revizyonunu siler.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Bir "silme" revizyonu:
// Bu revizyon, değişiklikleri izlerken metni sildiğimizde meydana gelir. Metni bu şekilde sildiğimizde,
// revizyonu kabul edene kadar belgede bir revizyon olarak kalacaktır,
// ya metni tamamen silecek ya da revizyonu reddedecek, bu da sildiğimiz metni olduğu yerde tutacak.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ayrıca bakınız

* class [Inline](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
