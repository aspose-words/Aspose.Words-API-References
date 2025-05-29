---
title: Document.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: .NET için Aspose.Words
description: Gelişmiş aracımızla belge revizyonlarını zahmetsizce takip edin. Net, vurgulanmış değişikliklerle düzenli kalın ve iş birliğini geliştirin!
type: docs
weight: 370
url: /tr/net/aspose.words/document/revisions/
---
## Document.Revisions property

Bu belgede bulunan revizyonların (izlenen değişikliklerin) bir koleksiyonunu alır.

```csharp
public RevisionCollection Revisions { get; }
```

## Notlar

Döndürülen koleksiyon "canlı" bir koleksiyondur; bu, bir belgenin revizyon içeren kısımlarını kaldırırsanız, silinen revizyonların bu koleksiyondan otomatik olarak kaybolacağı anlamına gelir.

## Örnekler

Bir belgedeki revizyonlarla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin normal düzenlenmesi revizyon olarak sayılmaz.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Düzenlemelerimizi revizyon olarak kaydetmek için bir yazar bildirmemiz ve ardından bunları izlemeye başlamamız gerekiyor.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Bu bayrak Microsoft Word'deki "İnceleme" -> "İzleme" -> "Değişiklikleri İzle" seçeneğine karşılık gelir.
// "StartTrackRevisions" yöntemi değerini etkilemez,
// ve belge "false" değerine sahip olmasına rağmen revizyonları programatik olarak izliyor.
// Bu belgeyi Microsoft Word kullanarak açarsak revizyonları izlemeyecektir.
Assert.IsFalse(doc.TrackRevisions);

// Belge oluşturucuyu kullanarak metin ekledik, bu nedenle ilk revizyon ekleme türünde bir revizyondur.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Silme tipi bir revizyon oluşturmak için bir çalışmayı kaldırın.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Yeni bir revizyon eklemek, onu revizyon koleksiyonunun başına yerleştirir.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Revizyon eklemeleri, revizyonu kabul/reddetmemizden önce bile belge gövdesinde görünür.
// Revizyonu reddetmek, onun düğümlerini gövdeden kaldıracaktır. Tersine, revizyonları oluşturan düğümler silinir
// Ayrıca, revizyonu kabul edene kadar belgede kalacaktır.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Silme revizyonunu kabul etmek, onun üst düğümünü paragraf metninden kaldıracaktır
// ve ardından koleksiyonun revizyonunu kaldırın.
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

// Taşınan revizyon artık 1. indekste. İçeriğini silmek için revizyonu reddedin.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [RevisionCollection](../../revisioncollection/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
