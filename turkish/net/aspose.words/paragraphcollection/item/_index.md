---
title: ParagraphCollection.Item
second_title: Aspose.Words for .NET API Referansı
description: ParagraphCollection mülk. Bir öğeyi alırParagraph verilen dizinde.
type: docs
weight: 10
url: /tr/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

Bir öğeyi alır[`Paragraph`](../../paragraph/) verilen dizinde.

```csharp
public Paragraph this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyona bir dizin. |

### Notlar

Endeks sıfır bazlıdır.

Negatif dizinlere izin verilir ve koleksiyonun arkasından erişimi belirtir. Örneğin -1 son öğe anlamına gelir, -2 sondan önceki ikinci öğe anlamına gelir ve bu şekilde devam eder.

Dizin listedeki öğe sayısından büyük veya ona eşitse bu, boş bir başvuru döndürür.

Dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse bu, boş bir başvuru döndürür.

### Örnekler

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

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* ad alanı [Aspose.Words](../../paragraphcollection/)
* toplantı [Aspose.Words](../../../)


