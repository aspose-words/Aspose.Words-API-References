---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartLegend för att förbättra dina diagram med anpassningsbara förklaringsegenskaper för bättre datavisualisering.
type: docs
weight: 1010
url: /sv/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Representerar egenskaper för diagramförklaring.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartLegend
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegend/font/) { get; } | Ger åtkomst till standardteckensnittsformateringen för förklaringsposter. För att åsidosätta teckensnittsformateringen för en specifik förklaringspost, använd[`Font`](../chartlegendentry/font/) egendom. |
| [Format](../../aspose.words.drawing.charts/chartlegend/format/) { get; } | Ger åtkomst till fyllnings- och linjeformatering av förklaringen. |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Returnerar en samling förklaringsposter för alla serier och trendlinjer i det överordnade diagrammet. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Avgör om andra diagramelement ska tillåtas överlappa förklaringen. Standardvärdet är`falsk` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Anger förklaringens position i ett diagram. |

## Exempel

Visar hur man redigerar utseendet på ett diagrams förklaring.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Flytta diagrammets förklaring till det övre högra hörnet.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Ge andra diagramelement, som grafen, mer utrymme genom att låta dem överlappa förklaringen.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
