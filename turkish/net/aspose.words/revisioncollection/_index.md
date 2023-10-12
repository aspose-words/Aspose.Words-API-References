---
title: Class RevisionCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.RevisionCollection sınıf. Bir koleksiyonRevision belgedeki revizyonları temsil eden nesneler.
type: docs
weight: 4770
url: /tr/net/aspose.words/revisioncollection/
---
## RevisionCollection class

Bir koleksiyon[`Revision`](../revision/) belgedeki revizyonları temsil eden nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgedeki Değişiklikleri İzleme](https://docs.aspose.com/words/net/track-changes-in-a-document/) dokümantasyon makalesi.

```csharp
public class RevisionCollection : IEnumerable<Revision>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/revisioncollection/count/) { get; } | Koleksiyondaki düzeltmelerin sayısını döndürür. |
| [Groups](../../aspose.words/revisioncollection/groups/) { get; } | Revizyon gruplarının toplanması. |
| [Item](../../aspose.words/revisioncollection/item/) { get; } | Bir değeri döndürür[`Revision`](../revision/) belirtilen dizinde. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [AcceptAll](../../aspose.words/revisioncollection/acceptall/)() | Bu koleksiyondaki tüm revizyonları kabul eder. |
| [GetEnumerator](../../aspose.words/revisioncollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |
| [RejectAll](../../aspose.words/revisioncollection/rejectall/)() | Bu koleksiyondaki tüm düzeltmeleri reddeder. |

### Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Kullan[`Revisions`](../document/revisions/) Bir belgede revizyonların bulunmasını sağlayan özellik.

### Örnekler

Bir belgedeki düzeltmelerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dokümanın normal şekilde düzenlenmesi revizyon olarak sayılmaz.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Düzenlemelerimizi revizyon olarak kaydetmek için bir yazar bildirmemiz ve ardından bunları izlemeye başlamamız gerekiyor.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Bu bayrak "İnceleme"ye karşılık gelir -> "İzleme" -> Microsoft Word'deki "Değişiklikleri İzle" seçeneği.
// "StartTrackRevisions" yöntemi değerini etkilemez,
// ve belge "yanlış" değerine sahip olmasına rağmen programlı olarak revizyonları izliyor.
// Bu belgeyi Microsoft Word kullanarak açarsak revizyon takibi olmayacaktır.
Assert.IsFalse(doc.TrackRevisions);

// Belge oluşturucuyu kullanarak metin ekledik, dolayısıyla ilk revizyon ekleme tipi bir revizyondur.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Silme tipi bir revizyon oluşturmak için bir çalıştırmayı kaldırın.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Yeni bir revizyon eklemek onu revizyon koleksiyonunun başına yerleştirir.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Düzeltmeleri kabul etmeden/reddetmeden önce bile belge gövdesinde düzeltmeleri ekleyin.
// Revizyonun reddedilmesi, düğümlerinin gövdeden kaldırılmasına neden olacaktır. Bunun tersine, silme revizyonlarını oluşturan düğümler
// ayrıca revizyonu kabul edene kadar belgede oyalanacağız.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Silme düzeltmesini kabul etmek, onun üst düğümünü paragraf metninden kaldıracaktır
// ve ardından koleksiyonun revizyonunun kendisini kaldırın.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Şimdi hareketli bir revizyon türü oluşturmak için düğümü taşıyın.
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// Hareket eden revizyon şu anda dizin 1'de. İçeriğini atmak için revizyonu reddedin.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Revision](../revision/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


