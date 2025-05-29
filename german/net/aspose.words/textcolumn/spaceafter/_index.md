---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words für .NET
description: Entdecken Sie die TextColumn SpaceAfter-Eigenschaft, um den Abstand zwischen Spalten in Ihrem Layout einfach anzupassen. Verbessern Sie Lesbarkeit und Design mit Präzision!
type: docs
weight: 10
url: /de/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Ruft den Abstand zwischen dieser und der nächsten Spalte in Punkten ab oder legt ihn fest. Für die letzte Spalte ist dies nicht erforderlich.

```csharp
public double SpaceAfter { get; set; }
```

## Beispiele

Zeigt, wie Spalten mit ungleichmäßigem Abstand erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Bestimmen Sie, wie viel Platz uns zum Anordnen der Spalten zur Verfügung steht.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Legen Sie fest, dass die erste Spalte schmal ist.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Stellen Sie die zweite Spalte so ein, dass sie den restlichen verfügbaren Platz innerhalb der Seitenränder einnimmt.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Siehe auch

* class [TextColumn](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
