---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: ParagraphCollection Item özelliğiyle belirli Paragraflara kolayca erişin. Sorunsuz metin yönetimi için herhangi bir Paragrafı dizine göre alın.
type: docs
weight: 10
url: /tr/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

Birini alır[`Paragraph`](../../paragraph/) verilen indekste.

```csharp
public Paragraph this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyonun indeksi. |

## Notlar

Endeks sıfır bazlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi belirtir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

Eğer indeks listedeki öğe sayısından büyük veya eşitse, bu boş bir referans döndürür.

Eğer indeks negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu durum boş bir referans döndürür.

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

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
