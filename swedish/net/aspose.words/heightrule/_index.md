---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.HeightRule enum för exakt kontroll över objekthöjd i dokument. Optimera ditt arbetsflöde med denna viktiga funktion!
type: docs
weight: 3560
url: /sv/net/aspose.words/heightrule/
---
## HeightRule enumeration

Anger regeln för att bestämma ett objekts höjd.

```csharp
public enum HeightRule
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| AtLeast | `0` | Höjden kommer att vara minst den angivna höjden i punkter. Den kommer att öka, om det behövs, för att rymma all text inuti ett objekt. |
| Exactly | `1` | Höjden anges exakt i punkter. Observera att om texten inte kan få plats inuti objektet med denna höjd kommer den att visas avkortad. |
| Auto | `2` | Höjden ökar automatiskt för att få plats med all text inuti ett objekt. |

## Exempel

Visar hur man formaterar rader med en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Starta en andra rad och konfigurera sedan dess höjd. Byggaren kommer att tillämpa dessa inställningar på
// dess nuvarande rad, såväl som alla nya rader som skapas efteråt.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Den första raden påverkades inte av omkonfigureringen av utfyllnaden och har fortfarande standardvärdena.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
