---
title: TextColumnCollection.LineBetween
linktitle: LineBetween
articleTitle: LineBetween
second_title: Aspose.Words för .NET
description: TextColumnCollection LineBetween fast egendom. NärSann lägger till en vertikal linje mellan kolumner i C#.
type: docs
weight: 40
url: /sv/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

När`Sann` lägger till en vertikal linje mellan kolumner.

```csharp
public bool LineBetween { get; set; }
```

## Exempel

Visar hur man separerar kolumner med en vertikal linje.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Konfigurera det aktuella avsnittets PageSetup-objekt för att dela upp texten i flera kolumner.
// Ställ in egenskapen "LineBetween" till "true" för att sätta en skiljelinje mellan kolumner.
// Ställ in egenskapen "LineBetween" till "false" för att lämna mellanrummet mellan kolumnerna tomt.
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.LineBetween = lineBetween;
columns.SetCount(3);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 3.");

doc.Save(ArtifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### Se även

* class [TextColumnCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
