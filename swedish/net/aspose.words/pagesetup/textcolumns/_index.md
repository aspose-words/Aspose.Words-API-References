---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words för .NET
description: PageSetup TextColumns fast egendom. Returnerar en samling som representerar uppsättningen textkolumner i C#.
type: docs
weight: 420
url: /sv/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Returnerar en samling som representerar uppsättningen textkolumner.

```csharp
public TextColumnCollection TextColumns { get; }
```

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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
