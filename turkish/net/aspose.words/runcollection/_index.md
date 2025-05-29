---
title: RunCollection Class
linktitle: RunCollection
articleTitle: RunCollection
second_title: .NET için Aspose.Words
description: Run düğümlerine sorunsuz erişim için Aspose.Words.RunCollection sınıfını keşfedin. Güçlü, yazılmış özelliklerle belge işlemenizi geliştirin!
type: docs
weight: 5570
url: /tr/net/aspose.words/runcollection/
---
## RunCollection class

Bir koleksiyona yazılmış erişim sağlar[`Run`](../run/) düğümler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public class RunCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/runcollection/item/) { get; } | Birini alır[`Run`](../run/) verilen indekste. (2 indexers) |

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
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Koleksiyondaki tüm çalıştırmaları yeni bir çalıştırma dizisine kopyalar. (2 methods) |

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

* class [NodeCollection](../nodecollection/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
