---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TextColumnCollection Spacing, hantera enkelt kolumnavstånd i punkter för en elegant och professionell layout. Förbättra din design idag!
type: docs
weight: 50
url: /sv/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

När kolumnerna är jämnt fördelade, hämtar eller ställer in mängden avstånd mellan varje kolumn i punkter.

```csharp
public double Spacing { get; set; }
```

## Anmärkningar

Gäller endast när[`EvenlySpaced`](../evenlyspaced/) är inställd på`sann` .

## Exempel

Visar hur man skapar flera jämnt fördelade kolumner i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Se även

* class [TextColumnCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
