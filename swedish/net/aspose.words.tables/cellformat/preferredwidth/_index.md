---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CellFormat PreferredWidth för att enkelt anpassa cellbredder för optimal layout och design i dina kalkylblad. Förbättra din datapresentation!
type: docs
weight: 80
url: /sv/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Returnerar eller anger önskad cellbredd.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Anmärkningar

Den önskade bredden (tillsammans med tabellens alternativ för automatisk anpassning) avgör hur cellens faktiska bredd beräknas av tabellens layoutalgoritm. Tabelllayout kan utföras av Aspose.Words när dokumentet sparas eller av Microsoft Word när dokumentet visas.

Den önskade bredden kan anges i punkter eller i procent. Den önskade width kan också anges som "auto", vilket innebär att ingen önskad bredd anges.

Standardvärdet är[`Auto`](../../preferredwidth/auto/).

## Exempel

Visar hur man anger en önskad bredd för tabellceller.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Det finns två sätt att tillämpa klassen "PreferredWidth" på tabellceller.
// 1 - Ange en absolut önskad bredd baserat på punkter:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Ange en relativ önskad bredd baserat på procentandel av tabellens bredd:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// En cell utan specificerad önskad bredd kommer att ta upp resten av det tillgängliga utrymmet.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Varje konfiguration av egenskapen "PreferredWidth" skapar ett nytt objekt.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Se även

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
