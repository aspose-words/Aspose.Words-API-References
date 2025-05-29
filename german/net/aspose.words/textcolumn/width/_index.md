---
title: TextColumn.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words für .NET
description: Passen Sie die Eigenschaft „TextColumn Width“ an, um die Breite Ihrer Textspalte in Punkten einfach anzupassen und so die Layoutkontrolle und Lesbarkeit zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words/textcolumn/width/
---
## TextColumn.Width property

Ruft die Breite der Textspalte in Punkten ab oder legt sie fest.

```csharp
public double Width { get; set; }
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
