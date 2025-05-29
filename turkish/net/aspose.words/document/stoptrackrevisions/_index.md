---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: .NET için Aspose.Words
description: Otomatik belge değişikliği işaretlemelerini önlemek, düzenleme verimliliğinizi ve belge netliğinizi artırmak için StopTrackRevisions yöntemini nasıl kullanacağınızı öğrenin.
type: docs
weight: 770
url: /tr/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Belge değişikliklerinin revizyon olarak otomatik olarak işaretlenmesini durdurur.

```csharp
public void StopTrackRevisions()
```

## Örnekler

Bir belgeyi düzenlerken revizyonların nasıl izleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir belgenin düzenlenmesi, genellikle onları izlemeye başlayana kadar bir revizyon olarak sayılmaz.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Gelecekteki düzenlemelerin revizyon olarak sayılmaması için revizyonları izlemeyi bırakın.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Revizyonlar oluşturulduğunda, onlara işlemin tarihi ve saati verilir.
// Revizyonları izlemeye başladığımızda DateTime.MinValue değerini geçirerek bunu devre dışı bırakabiliriz.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Bu revizyonları programatik olarak kabul edebilir/reddedebiliriz
// Document.AcceptAllRevisions gibi yöntemleri veya her revizyonun Accept yöntemini çağırarak.
// Microsoft Word'de bunları "Gözden Geçir" -> "Değişiklikler" yoluyla manuel olarak işleyebiliriz.
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Ayrıca bakınız

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
