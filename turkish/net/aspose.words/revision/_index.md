---
title: Revision
second_title: Aspose.Words for .NET API Referansı
description: Bir belge düğümünde veya stilinde bir revizyonu izlenen değişiklik temsil eder. KullanımRevisionType./revision/revisiontype/ bu revizyonun türünü kontrol etmek için.
type: docs
weight: 4500
url: /tr/net/aspose.words/revision/
---
## Revision class

Bir belge düğümünde veya stilinde bir revizyonu (izlenen değişiklik) temsil eder. Kullanım[`RevisionType`](./revisiontype/) bu revizyonun türünü kontrol etmek için.

```csharp
public class Revision
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | Bu düzeltmenin yazarını alır veya ayarlar. Boş dize veya null olamaz. |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | Bu düzeltmenin tarihini/saatini alır veya ayarlar. |
| [Group](../../aspose.words/revision/group/) { get; } | Revizyon grubunu alır. Revizyon herhangi bir gruba ait değilse null döndürür. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | Bu revizyonun hemen üst düğümünü (sahibini) alır. Bu özellik, aşağıdakiler dışındaki herhangi bir revizyon türü için çalışacaktır.StyleDefinitionChange . |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | Bu revizyonun hemen üst stilini (sahibini) alır. Bu özellik yalnızcaStyleDefinitionChange revizyon türü. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | Bu düzeltmenin türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | Bu düzeltmeyi kabul eder. |
| [Reject](../../aspose.words/revision/reject/)() | Bu düzeltmeyi reddet. |

### Örnekler

Bir belgedeki revizyonlarla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin normal düzenlenmesi revizyon sayılmaz.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Düzenlemelerimizi revizyon olarak kaydetmek için bir yazar bildirmemiz ve ardından onları izlemeye başlamamız gerekiyor.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Bu bayrak "İnceleme" -> "İzleme" -> Microsoft Word'de "Değişiklikleri İzle" seçeneği.
// "StartTrackRevisions" yöntemi değerini etkilemez,
// ve belge, "yanlış" değerine sahip olmasına rağmen, revizyonları programlı olarak izliyor.
// Bu belgeyi Microsoft Word kullanarak açarsak, revizyonları izlemeyecektir.
Assert.IsFalse(doc.TrackRevisions);

// Belge oluşturucuyu kullanarak metin ekledik, bu nedenle ilk revizyon ekleme tipi bir revizyondur.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Silme tipi bir revizyon oluşturmak için bir çalıştırmayı kaldırın.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Yeni bir revizyon eklemek, onu revizyon koleksiyonunun başına yerleştirir.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Revizyonları, biz revizyonu kabul etmeden/reddetmeden önce bile belge gövdesinde görünüyor.
// Revizyonu reddetmek, düğümlerini gövdeden kaldırır. Tersine, silme revizyonlarını oluşturan düğümler
// ayrıca revizyonu kabul edene kadar belgede oyalanır.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Silme revizyonunu kabul etmek, üst düğümünü paragraf metninden kaldıracak
// ve ardından koleksiyonun revizyonunun kendisini kaldırın.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Şimdi hareketli bir revizyon tipi oluşturmak için düğümü hareket ettirin.
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

// Hareketli revizyon şimdi 1. indekste. İçeriğini atmak için revizyonu reddet.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
