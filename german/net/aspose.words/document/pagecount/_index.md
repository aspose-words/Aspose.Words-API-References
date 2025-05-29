---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Document PageCount“, die die Gesamtseitenzahl basierend auf dem neuesten Layout anzeigt und so eine genaue Dokumentenverwaltung und Einblicke gewährleistet.
type: docs
weight: 330
url: /de/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Ruft die Anzahl der Seiten im Dokument ab, die durch den letzten Seitenlayoutvorgang berechnet wurde.

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

// Durch Abrufen der PageCount-Eigenschaft wurde das Seitenlayout des Dokuments aufgerufen, um den Wert zu berechnen.
// Dieser Vorgang muss nicht erneut ausgeführt werden, wenn das Dokument in ein festes Seitenspeicherformat gerendert wird.
// wie z.B. .pdf. So können Sie gerade bei komplexeren Dokumenten etwas Zeit sparen.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Siehe auch

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
