---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Tables.TextWrapping-enum för effektiv textbrytning runt tabeller. Förbättra din dokumentformatering med lätthet!
type: docs
weight: 7230
url: /sv/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

Anger hur text radbryts runt tabellen.

```csharp
public enum TextWrapping
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Text och tabell visas i den ordning de visas i dokumentet. |
| Around | `1` | Texten radbryts runt tabellen och upptar tillgängligt sidoutrymme. |
| Default | `0` | Standardvärde. |

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

// Sätt egenskapen "TextWrapping" till "TextWrapping.Around" för att få tabellen att radbryta text runt den,
// och tryck ner den i stycket nedan genom att ange positionen.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Se även

* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
