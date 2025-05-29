---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.ChartDataLabelPosition-uppräkningen för att enkelt anpassa dina diagramdataetiketter för förbättrad tydlighet och presentation.
type: docs
weight: 960
url: /sv/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

Anger positionen för en diagramdataetikett.

```csharp
public enum ChartDataLabelPosition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Center | `0` | Anger att en dataetikett ska visas centrerad på en datamarkör. |
| Left | `1` | Anger att en dataetikett ska visas till vänster om en datamarkör. |
| Right | `2` | Anger att en dataetikett ska visas till höger om en datamarkör. |
| Above | `3` | Anger att en dataetikett ska visas ovanför en datamarkör. |
| Below | `4` | Anger att en dataetikett ska visas under en datamarkör. |
| InsideBase | `5` | Anger att en dataetikett ska visas inuti basen av en datamarkör. |
| InsideEnd | `6` | Anger att en dataetikett ska visas i slutet av en datamarkör. |
| OutsideEnd | `7` | Anger att en dataetikett ska visas utanför slutet av en datamarkör. |
| BestFit | `8` | Anger att en dataetikett ska visas på den mest lämpliga positionen. |

## Anmärkningar

Inte alla serietyper tillåter angivande av etikettpositioner. Och de som gör det stöder inte alla värden.

## Exempel

Visar hur man ställer in positionen för dataetiketten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga kolumndiagram.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Radera standardgenererad serie.
seriesColl.Clear();

// Lägg till serie.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Visa dataetiketter och ange teckenfärg.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Ange dataetikettens position.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
