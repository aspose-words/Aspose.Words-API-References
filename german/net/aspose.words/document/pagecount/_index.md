---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words für .NET
description: Document PageCount eigendom. Ruft die Anzahl der Seiten im Dokument ab wie durch den letzten SeitenlayoutVorgang berechnet in C#.
type: docs
weight: 320
url: /de/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Ruft die Anzahl der Seiten im Dokument ab, wie durch den letzten Seitenlayout-Vorgang berechnet.

```csharp
public int PageCount { get; }
```

## Beispiele

Zeigt, wie die Anzahl der Seiten im Dokument gezählt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Überprüfen Sie die erwartete Seitenzahl des Dokuments.
Assert.AreEqual(3, doc.PageCount);

// Beim Abrufen der PageCount-Eigenschaft wurde das Seitenlayout des Dokuments aufgerufen, um den Wert zu berechnen.
// Dieser Vorgang muss nicht erneut durchgeführt werden, wenn das Dokument in einem festen Seitenspeicherformat gerendert wird.
// wie .pdf. So können Sie gerade bei komplexeren Dokumenten einiges an Zeit sparen.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Siehe auch

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
