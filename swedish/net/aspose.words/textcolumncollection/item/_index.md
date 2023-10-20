---
title: TextColumnCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: TextColumnCollection Item fast egendom. Returnerar en textkolumn vid det angivna indexet i C#.
type: docs
weight: 30
url: /sv/net/aspose.words/textcolumncollection/item/
---
## TextColumnCollection indexer

Returnerar en textkolumn vid det angivna indexet.

```csharp
public TextColumn this[int index] { get; }
```

## Exempel

Visar hur man skapar ojämnt fördelade kolumner.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Bestäm mängden utrymme som vi har tillgängligt för att arrangera kolumner.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Ange att den första kolumnen ska vara smal.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Ställ in den andra kolumnen för att ta resten av det tillgängliga utrymmet inom sidans marginaler.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Se även

* class [TextColumn](../../textcolumn/)
* class [TextColumnCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
