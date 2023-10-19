---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words for .NET
description: Document StopTrackRevisions yöntem. Belge değişikliklerinin otomatik olarak revizyon olarak işaretlenmesini durdurur C#'da.
type: docs
weight: 720
url: /tr/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Belge değişikliklerinin otomatik olarak revizyon olarak işaretlenmesini durdurur.

```csharp
public void StopTrackRevisions()
```

## Örnekler

Bir belgeyi düzenlerken revizyonların nasıl izleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir belgeyi düzenlemek genellikle biz onu izlemeye başlayana kadar revizyon olarak sayılmaz.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Gelecekteki düzenlemeleri revizyon olarak saymamak için revizyonları izlemeyi durdurun.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Revizyonların oluşturulması onlara işlemin tarihini ve saatini verir.
// Revizyonları izlemeye başladığımızda DateTime.MinValue'yu ileterek bunu devre dışı bırakabiliriz.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Bu revizyonları programlı olarak kabul edebilir/reddedebiliriz
// Document.AcceptAllRevisions gibi yöntemleri veya her revizyonun Accept yöntemini çağırarak.
// Microsoft Word'de bunları "İncele" -> aracılığıyla manuel olarak işleyebiliriz. "Değişiklikler".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Ayrıca bakınız

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
