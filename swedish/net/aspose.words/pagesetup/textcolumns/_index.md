---
title: PageSetup.TextColumns
second_title: Aspose.Words för .NET API Referens
description: PageSetup fast egendom. Returnerar en samling som representerar uppsättningen textkolumner.
type: docs
weight: 420
url: /sv/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Returnerar en samling som representerar uppsättningen textkolumner.

```csharp
public TextColumnCollection TextColumns { get; }
```

### Exempel

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
* namnutrymme [Aspose.Words](../../pagesetup/)
* hopsättning [Aspose.Words](../../../)


