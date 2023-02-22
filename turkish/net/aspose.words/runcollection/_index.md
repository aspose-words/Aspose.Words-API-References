---
title: Class RunCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.RunCollection sınıf. Bir koleksiyona yazılı erişim sağlarRun düğümler.
type: docs
weight: 4570
url: /tr/net/aspose.words/runcollection/
---
## RunCollection class

Bir koleksiyona yazılı erişim sağlar[`Run`](../run/) düğümler.

```csharp
public class RunCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/runcollection/item/) { get; } | Bir **Koşmak** verilen dizinde. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Koleksiyonda bir düğüm olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" stili yineleme sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Belirtilen dizindeki koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Koleksiyondaki tüm çalıştırmaları yeni bir çalıştırma dizisine kopyalar. (2 methods) |

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

* class [NodeCollection](../nodecollection/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


