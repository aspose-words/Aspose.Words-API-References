---
title: Revision Class
linktitle: Revision
articleTitle: Revision
second_title: Aspose.Words for .NET
description: Aspose.Words.Revision sınıf. Bir belge düğümünde veya stilinde bir revizyonu izlenen değişiklik temsil eder. KullanımRevisionType bu revizyonun türünü kontrol etmek için C#'da.
type: docs
weight: 4760
url: /tr/net/aspose.words/revision/
---
## Revision class

Bir belge düğümünde veya stilinde bir revizyonu (izlenen değişiklik) temsil eder. Kullanım[`RevisionType`](./revisiontype/) bu revizyonun türünü kontrol etmek için.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgedeki Değişiklikleri İzleme](https://docs.aspose.com/words/net/track-changes-in-a-document/) dokümantasyon makalesi.

```csharp
public class Revision
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | Bu düzeltmenin yazarını alır veya ayarlar. Boş dize olamaz veya`hükümsüz` . |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | Bu düzeltmenin tarihini/saatini alır veya ayarlar. |
| [Group](../../aspose.words/revision/group/) { get; } | Revizyon grubunu alır. İadeler`hükümsüz` revizyon herhangi bir gruba ait değilse. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | Bu revizyonun doğrudan üst düğümünü (sahibini) alır. Bu özellik, aşağıdakiler dışındaki tüm revizyon türleri için çalışacaktır:StyleDefinitionChange . |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | Bu revizyonun doğrudan ana stilini (sahibini) alır. Bu özellik yalnızcaStyleDefinitionChange revizyon tipi. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | Bu revizyonun türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | Bu düzeltmeyi kabul eder. |
| [Reject](../../aspose.words/revision/reject/)() | Bu düzeltmeyi reddet. |

## Örnekler

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
