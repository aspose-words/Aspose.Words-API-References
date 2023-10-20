---
title: RunCollection Class
linktitle: RunCollection
articleTitle: RunCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.RunCollection sınıf. Bir koleksiyona yazılı erişim sağlarRun düğümler C#'da.
type: docs
weight: 4830
url: /tr/net/aspose.words/runcollection/
---
## RunCollection class

Bir koleksiyona yazılı erişim sağlar[`Run`](../run/) düğümler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

```csharp
public class RunCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/runcollection/item/) { get; } | Bir öğeyi alır[`Run`](../run/) verilen dizinde. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tüm düğümleri bu koleksiyondan ve belgeden kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğümlerin koleksiyonu üzerinde basit bir "foreach" stili yinelemesi sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Belirtilen dizindeki koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Koleksiyondaki tüm çalıştırmaları yeni bir çalıştırma dizisine kopyalar. (2 methods) |

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

* class [NodeCollection](../nodecollection/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
