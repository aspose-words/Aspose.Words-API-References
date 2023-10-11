---
title: Enum RevisionType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.RevisionType Sıralama. İzlenen değişikliğin türünü belirtirRevision .
type: docs
weight: 4800
url: /tr/net/aspose.words/revisiontype/
---
## RevisionType enumeration

İzlenen değişikliğin türünü belirtir[`Revision`](../revision/) .

```csharp
public enum RevisionType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Insertion | `0` | Belgeye yeni içerik eklendi. |
| Deletion | `1` | İçerik belgeden kaldırıldı. |
| FormatChange | `2` | Üst düğüme biçimlendirme değişikliği uygulandı. |
| StyleDefinitionChange | `3` | Ana stile biçimlendirme değişikliği uygulandı. |
| Moving | `4` | İçerik belgeye taşındı. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


