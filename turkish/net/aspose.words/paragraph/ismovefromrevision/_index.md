---
title: Paragraph.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words for .NET
description: Paragraph IsMoveFromRevision mülk. İadelerdoğru değişiklik izleme etkinken bu nesne Microsoft Wordde taşındıysa silindiyse C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words/paragraph/ismovefromrevision/
---
## Paragraph.IsMoveFromRevision property

İadeler`doğru` değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse).

```csharp
public bool IsMoveFromRevision { get; }
```

## Örnekler

Bir paragrafın taşıma düzeltmesi olup olmadığının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Bu belge, metni imleçle vurguladığımızda görünen "Taşı" revizyonlarını içerir,
// ve ardından başka bir konuma taşımak için sürükleyin
// "İnceleme" aracılığıyla Microsoft Word'deki revizyonları izlerken -> "Parça değişiklikleri".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Revizyonları taşıma, "Şuraya Taşı" ve "Şuraya Taşı" revizyon çiftlerinden oluşur.
// Bu revizyonlar, belgede kabul edebileceğimiz veya reddedebileceğimiz potansiyel değişikliklerdir.
// Bir taşıma revizyonunu kabul etmeden/reddetmeden önce belge
// metnin hem kalkış hem de varış yerlerini takip etmelidir.
// İkinci ve dördüncü paragraf böyle bir revizyonu tanımlar ve dolayısıyla her ikisi de aynı içeriğe sahiptir.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// "Taşı" revizyonu, metni sürüklediğimiz paragraftır.
// Eğer revizyonu kabul edersek bu paragraf kaybolacak,
// ve diğeri kalacak ve artık revizyon olmayacak.
Assert.True(paragraphs[1].IsMoveFromRevision);

// "Taşı" revizyonu, metni sürüklediğimiz paragraftır.
// Eğer revizyonu reddedersek, bu paragraf kaybolacak ve diğeri kalacaktır.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
