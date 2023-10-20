---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words för .NET
description: Aspose.Words.HeightRule uppräkning. Anger regeln för att bestämma höjden på ett objekt i C#.
type: docs
weight: 3130
url: /sv/net/aspose.words/heightrule/
---
## HeightRule enumeration

Anger regeln för att bestämma höjden på ett objekt.

```csharp
public enum HeightRule
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| AtLeast | `0` | Höjden kommer att vara minst den angivna höjden i poäng. Det kommer att växa, om det behövs, för att rymma all text inuti ett objekt. |
| Exactly | `1` | Höjden anges exakt i punkter. Observera att om texten inte kan passa inuti objektet med denna höjd, kommer den att se trunkerad ut. |
| Auto | `2` | Höjden växer automatiskt för att rymma all text inuti ett objekt. |

## Exempel

Visar hur man formaterar rader med en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Starta en andra rad och konfigurera sedan dess höjd. Byggaren kommer att tillämpa dessa inställningar på
// dess nuvarande rad, såväl som alla nya rader som den skapar efteråt.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Den första raden påverkades inte av utfyllnadsomställningen och har fortfarande standardvärdena.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
