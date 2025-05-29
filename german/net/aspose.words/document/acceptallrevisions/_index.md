---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Bearbeitungsprozess mit der Methode „AcceptAllRevisions“ und akzeptieren Sie mühelos alle nachverfolgten Änderungen in Ihrem Dokument für eine ausgefeilte Endversion.
type: docs
weight: 540
url: /de/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Akzeptiert alle nachverfolgten Änderungen im Dokument.

```csharp
public void AcceptAllRevisions()
```

## Bemerkungen

Diese Methode ist eine Abkürzung für[`AcceptAll`](../../revisioncollection/acceptall/).

## Beispiele

Zeigt, wie alle nachverfolgten Änderungen im Dokument akzeptiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bearbeiten Sie das Dokument, während Sie die Änderungen verfolgen, um einige Revisionen zu erstellen.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! ");
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Wir können jede Revision durchlaufen und sie als Teil unseres Dokuments akzeptieren/ablehnen.
// Wenn wir wissen, dass wir jede Revision akzeptieren möchten, können wir dies einfacher tun, indem wir diese Methode aufrufen.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
