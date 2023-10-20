---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words für .NET
description: TextColumn SpaceAfter eigendom. Ruft den Abstand zwischen dieser Spalte und der nächsten Spalte in Punkten ab oder legt diesen fest. Für die letzte Spalte nicht erforderlich in C#.
type: docs
weight: 10
url: /de/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Ruft den Abstand zwischen dieser Spalte und der nächsten Spalte in Punkten ab oder legt diesen fest. Für die letzte Spalte nicht erforderlich.

```csharp
public double SpaceAfter { get; set; }
```

## Beispiele

Zeigt, wie ungleichmäßig verteilte Spalten erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Bestimmen Sie den verfügbaren Platz für die Anordnung der Spalten.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Setze die erste Spalte auf schmal.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Legen Sie die zweite Spalte so fest, dass sie den Rest des verfügbaren Platzes innerhalb der Seitenränder einnimmt.
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
