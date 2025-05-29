---
title: Paragraph.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: .NET için Aspose.Words
description: Microsoft Word'deki IsMoveToRevision özelliğini keşfedin! Değişiklikleri nasıl izlediğini ve belge düzenleme deneyiminizi nasıl geliştirdiğini öğrenin.
type: docs
weight: 140
url: /tr/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

Geri Döndürür`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinleştirilmişken taşınırsa (eklenirse).

```csharp
public bool IsMoveToRevision { get; }
```

## Örnekler

Bir paragrafın taşıma revizyonu olup olmadığının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Bu belge, metni imleçle vurguladığımızda görünen "Taşı" revizyonlarını içerir.
// ve sonra onu başka bir yere taşımak için sürükleyin
// Microsoft Word'de revizyonları "Gözden Geçir" -> "Değişiklikleri İzle" yoluyla izlerken.
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Revizyonları taşıma, "Şuradan taşı" ve "Şuraya taşı" revizyon çiftlerinden oluşur.
// Bu revizyonlar, belgede kabul edebileceğimiz veya reddedebileceğimiz potansiyel değişikliklerdir.
// Bir taşıma revizyonunu kabul etmeden/reddetmeden önce, belge
// Metnin hem kalkış hem de varış noktalarını takip etmek gerekir.
// İkinci ve dördüncü paragraflar böyle bir revizyonu tanımlıyor ve dolayısıyla her ikisinin de içeriği aynı.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// "Şuradan taşı" revizyonu, metni sürüklediğimiz paragraftır.
// Revizyonu kabul edersek bu paragraf kaybolacak,
// ve diğeri kalacak ve artık bir revizyon olmayacak.
Assert.True(paragraphs[1].IsMoveFromRevision);

// "Taşı" revizyonu, metni sürüklediğimiz paragraftır.
// Eğer revizyonu reddedersek, bu paragraf ortadan kalkacak ve diğeri kalacaktır.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
