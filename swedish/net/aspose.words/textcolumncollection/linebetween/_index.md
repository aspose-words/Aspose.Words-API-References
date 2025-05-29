---
title: TextColumnCollection.LineBetween
linktitle: LineBetween
articleTitle: LineBetween
second_title: Aspose.Words för .NET
description: Förbättra din layout med egenskapen TextColumnCollection LineBetween. Aktivera vertikala linjer mellan kolumner för ett elegant och organiserat utseende.
type: docs
weight: 40
url: /sv/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

När`sann` , lägger till en vertikal linje mellan kolumner.

```csharp
public bool LineBetween { get; set; }
```

## Exempel

Visar hur man separerar kolumner med en vertikal linje.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Konfigurera den aktuella sektionens PageSetup-objekt för att dela upp texten i flera kolumner.
// Sätt egenskapen "LineBetween" till "true" för att lägga till en skiljelinje mellan kolumner.
// Sätt egenskapen "LineBetween" till "false" för att lämna mellanrummet mellan kolumnerna tomt.
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
