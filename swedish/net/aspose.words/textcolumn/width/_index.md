---
title: TextColumn.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words för .NET
description: Justera egenskapen TextColumn Width för att enkelt anpassa textkolumnens bredd i punkter för förbättrad layoutkontroll och läsbarhet.
type: docs
weight: 20
url: /sv/net/aspose.words/textcolumn/width/
---
## TextColumn.Width property

Hämtar eller ställer in bredden på textkolumnen i punkter.

```csharp
public double Width { get; set; }
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
