---
title: Class ParagraphCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ParagraphCollection sınıf. Bir koleksiyona yazılı erişim sağlarParagraph düğümler.
type: docs
weight: 4410
url: /tr/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Bir koleksiyona yazılı erişim sağlar[`Paragraph`](../paragraph/) düğümler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Paragraflarla Çalışmak](https://docs.aspose.com/words/net/working-with-paragraphs/) dokümantasyon makalesi.

```csharp
public class ParagraphCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Bir öğeyi alır[`Paragraph`](../paragraph/) verilen dizinde. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tüm düğümleri bu koleksiyondan ve belgeden kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğümlerin koleksiyonu üzerinde basit bir "foreach" stili yinelemesi sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Belirtilen dizindeki koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Koleksiyondaki tüm paragrafları yeni bir paragraf dizisine kopyalar. (2 methods) |

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

* class [NodeCollection](../nodecollection/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


