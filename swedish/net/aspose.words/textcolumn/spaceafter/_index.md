---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TextColumn SpaceAfter för att enkelt justera avståndet mellan kolumner i din layout. Förbättra läsbarhet och design med precision!
type: docs
weight: 10
url: /sv/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Hämtar eller ställer in avståndet mellan denna kolumn och nästa kolumn i punkter. Krävs inte för den sista kolumnen.

```csharp
public double SpaceAfter { get; set; }
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

// Bestäm hur mycket utrymme vi har tillgängligt för att arrangera kolumner.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Sätt den första kolumnen till att vara smal.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Ställ in den andra kolumnen så att den tar upp resten av det tillgängliga utrymmet inom sidans marginaler.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Se även

* class [TextColumn](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
