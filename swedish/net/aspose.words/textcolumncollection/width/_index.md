---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TextColumnCollection Width. Hantera enkelt jämnt fördelade kolumner för optimal layout och design i dina projekt.
type: docs
weight: 60
url: /sv/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

När kolumnerna är jämnt fördelade, hämtar kolumnernas bredd.

```csharp
public double Width { get; }
```

## Anmärkningar

Har endast effekt när[`EvenlySpaced`](../evenlyspaced/) är inställd på`sann`.

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
