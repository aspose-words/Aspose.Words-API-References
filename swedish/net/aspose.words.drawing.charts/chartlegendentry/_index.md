---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ChartLegendEntry för att skapa dynamiska diagramförklaringar. Förbättra din datavisualisering med sömlös integration och anpassning.
type: docs
weight: 1020
url: /sv/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

Representerar en post i diagramförklaringen.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartLegendEntry
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | Ger åtkomst till teckensnittsformateringen för denna förklaring. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | Hämtar eller ställer in ett värde som anger om den här posten är dold i diagramförklaringen. Standardvärdet är**falsk** . |

## Anmärkningar

En förklaringspost motsvarar en specifik diagramserie eller trendlinje.

Texten i posten är namnet på serien eller trendlinjen. Texten kan inte ändras.

## Exempel

Visar hur man arbetar med ett teckensnitt för förklaringar.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Ange standardteckenstorlek för alla förklaringar.
chartLegend.Font.Size = 14;
// Ändra teckensnitt för specifik förklaring.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Hämta förklaringspost för diagramserier.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
