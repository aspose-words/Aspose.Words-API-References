---
title: ParagraphCollection Class
linktitle: ParagraphCollection
articleTitle: ParagraphCollection
second_title: .NET için Aspose.Words
description: Yapılandırılmış Paragraf düğümlerine kesintisiz erişim için Aspose.Words.ParagraphCollection'ı keşfedin, böylece projelerinizde belge düzenleme ve verimliliği artırın.
type: docs
weight: 5140
url: /tr/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Bir koleksiyona yazılmış erişim sağlar[`Paragraph`](../paragraph/) düğümler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Paragraflarla Çalışma](https://docs.aspose.com/words/net/working-with-paragraphs/) belgeleme makalesi.

```csharp
public class ParagraphCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Birini alır[`Paragraph`](../paragraph/) verilen indekste. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondan ve belgeden tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Belirtilen dizinde koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Koleksiyondaki tüm paragrafları yeni bir paragraf dizisine kopyalar. (2 methods) |

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

* class [NodeCollection](../nodecollection/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
