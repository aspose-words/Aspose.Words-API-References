---
title: Story.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: .NET için Aspose.Words
description: Hikaye Paragraflarını Keşfedin. Hikayenizden doğrudan seçilmiş bir paragraf koleksiyonuna erişin ve zengin, ilgi çekici içeriklerle anlatınızı zenginleştirin.
type: docs
weight: 30
url: /tr/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

Hikayenin doğrudan alt öğeleri olan paragrafların bir koleksiyonunu alır.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
