---
title: Inline.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words for .NET
description: Inline IsMoveToRevision mülk. İadelerdoğru bu nesne Microsoft Wordde değişiklik izleme etkinken taşınmışsa eklenmişse C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/inline/ismovetorevision/
---
## Inline.IsMoveToRevision property

İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse).

```csharp
public bool IsMoveToRevision { get; }
```

## Örnekler

Satır içi düğümün revizyon türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Belgeyi düzenlediğimizde, Gözden Geçirme yoluyla bulunan "Değişiklikleri İzle" seçeneği -> Takip,
// Microsoft Word'de açıldığında uyguladığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyonları izlemeye şu şekilde başlayabiliriz:
// belgenin "StartTrackRevisions" yöntemini çağırıyoruz ve "StopTrackRevisions" yöntemini kullanarak izlemeyi durduruyoruz.
// Belgeye asimile etmek için düzeltmeleri kabul edebiliriz
// veya önerilen değişikliği etkili bir şekilde değiştirmek için onları reddedin.
Assert.AreEqual(6, doc.Revisions.Count);

// Bir revizyonun ana düğümü, revizyonun ilgili olduğu çalıştırmadır. Çalıştırma bir Satır İçi düğümdür.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Aşağıda bir Satır İçi düğümü işaretleyebilen beş tür revizyon bulunmaktadır.
// 1 - Bir "ekleme" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metin eklediğimizde meydana gelir.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Bir "format" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metnin formatını değiştirdiğimizde ortaya çıkar.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Bir "şuradan taşıma" revizyonu:
// Microsoft Word'de metni vurgulayıp belgede farklı bir yere sürüklediğimizde
// Değişiklikleri takip ederken iki revizyon belirir.
// "Şuradan taşı" revizyonu, metnin biz taşımadan önceki orijinal kopyasıdır.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Bir "geçiş" revizyonu:
// "Taşı" revizyonu, belgedeki yeni konumuna taşıdığımız metindir.
// Gerçekleştirdiğimiz her hareket revizyonu için "Şuraya Taşı" ve "Şuraya Taşı" revizyonları çift olarak görünür.
// Bir taşıma revizyonunu kabul etmek, "şuradan taşıma" revizyonunu ve metnini siler,
// ve metni "şuraya taşı" revizyonundan korur.
// Bir taşıma revizyonunu reddetmek, tam tersine, "şuraya taşı" revizyonunu korur ve "şuraya taşı" revizyonunu siler.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Bir "silme" revizyonu:
// Değişiklikleri takip ederken metni sildiğimizde bu revizyon meydana gelir. Bunun gibi bir metni sildiğimizde,
// biz revizyonu kabul edene kadar belgede revizyon olarak kalacak,
// bu, metni tamamen silecek veya revizyonu reddedecek, bu da sildiğimiz metni olduğu yerde tutacak.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ayrıca bakınız

* class [Inline](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
