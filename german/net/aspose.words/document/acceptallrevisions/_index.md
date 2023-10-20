---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words für .NET
description: Document AcceptAllRevisions methode. Akzeptiert alle nachverfolgten Änderungen im Dokument in C#.
type: docs
weight: 520
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

Zeigt, wie alle Tracking-Änderungen im Dokument akzeptiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bearbeiten Sie das Dokument und verfolgen Sie dabei die Änderungen, um einige Überarbeitungen zu erstellen.
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
