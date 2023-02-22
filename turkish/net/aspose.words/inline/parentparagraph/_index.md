---
title: Inline.ParentParagraph
second_title: Aspose.Words for .NET API Referansı
description: Inline mülk. Üst öğeyi alırParagraph bu düğümün.
type: docs
weight: 70
url: /tr/net/aspose.words/inline/parentparagraph/
---
## Inline.ParentParagraph property

Üst öğeyi alır[`Paragraph`](../../paragraph/) bu düğümün.

```csharp
public Paragraph ParentParagraph { get; }
```

### Örnekler

Bir satır içi düğümün revizyon türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Belgeyi düzenlediğimizde "Değişiklikleri İzle" seçeneği, İnceleme -> izleme,
// Microsoft Word'de açık, uyguladığımız değişiklikler revizyon olarak sayılır.
// Aspose.Words kullanarak bir belgeyi düzenlerken, revizyonları şu şekilde izlemeye başlayabiliriz:
// belgenin "StartTrackRevisions" yöntemini çağırarak ve "StopTrackRevisions" yöntemini kullanarak izlemeyi durdurun.
// Revizyonları belgeye asimile etmek için kabul edebiliriz
// veya önerilen değişikliği etkili bir şekilde değiştirmek için onları reddedin.
Assert.AreEqual(6, doc.Revisions.Count);

// Bir revizyonun üst düğümü, revizyonun ilgili olduğu çalıştırmadır. Bir Çalıştırma, bir Satır içi düğümdür.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Aşağıda, bir Satır içi düğümü işaretleyebilen beş tür revizyon bulunmaktadır.
// 1 - Bir "insert" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metin eklediğimizde gerçekleşir.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Bir "biçim" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metnin formatını değiştirdiğimizde gerçekleşir.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Bir "geçiş" revizyonu:
// Microsoft Word'de metni vurgulayıp belgede farklı bir yere sürüklediğimizde
// değişiklikleri takip ederken iki revizyon görünür.
// "Move from" revizyonu, metnin biz onu taşımadan önceki orijinal kopyasıdır.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - "Taşı" revizyonu:
// "Taşı" revizyonu, belgedeki yeni konumuna taşıdığımız metindir.
// Yaptığımız her hareket revizyonu için "Move from" ve "move to" revizyonları çiftler halinde görünür.
// Bir taşıma revizyonunu kabul etmek, "move from" revizyonunu ve metnini siler,
// ve metni "move to" revizyonundan tutar.
// Bir taşıma revizyonunu reddetmek, tersine, "move from" revizyonunu korur ve "move to" revizyonunu siler.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Bir "sil" revizyonu:
// Bu revizyon, değişiklikleri takip ederken metni sildiğimizde gerçekleşir. Böyle bir metni sildiğimizde,
// biz revizyonu kabul edene kadar belgede revizyon olarak kalacak,
// metni tamamen silecek veya düzeltmeyi reddedecek, bu da sildiğimiz metni olduğu yerde tutacak.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [Inline](../)
* ad alanı [Aspose.Words](../../inline/)
* toplantı [Aspose.Words](../../../)


