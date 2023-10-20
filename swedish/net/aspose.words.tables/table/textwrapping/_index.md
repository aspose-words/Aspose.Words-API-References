---
title: Table.TextWrapping
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words för .NET
description: Table TextWrapping fast egendom. Hämtar eller sätterTextWrapping för tabell i C#.
type: docs
weight: 310
url: /sv/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Hämtar eller sätter`TextWrapping` för tabell.

```csharp
public TextWrapping TextWrapping { get; set; }
```

## Exempel

Visar hur man arbetar med tabelltextbrytning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Ställ in egenskapen "TextWrapping" till "TextWrapping.Around" för att få tabellen att linda text runt den,
// och tryck ner den i stycket nedan genom att ställa in positionen.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Se även

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
