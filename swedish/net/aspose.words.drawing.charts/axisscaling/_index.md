---
title: AxisScaling Class
linktitle: AxisScaling
articleTitle: AxisScaling
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.Charts.AxisScaling klass. Representerar skalningsalternativen för axeln i C#.
type: docs
weight: 570
url: /sv/net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

Representerar skalningsalternativen för axeln.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class AxisScaling
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [AxisScaling](axisscaling/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | Hämtar eller ställer in den logaritmiska basen för en logaritmisk axel. |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | Hämtar eller ställer in maxvärdet för axeln. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | Hämtar eller ställer in minimivärdet för axeln. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | Hämtar eller ställer in skalningstyp för axeln. |

## Exempel

Visar hur man tillämpar logaritmisk skalning på en diagramaxel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Infoga en serie med X/Y-koordinater för fem punkter.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// Skalningen av X-axeln är linjär som standard,
// visar jämnt ökande värden som täcker vårt X-värdeområde (0, 1, 2, 3...).
// En linjär axel är inte idealisk för våra Y-värden
// eftersom punkterna med de mindre Y-värdena blir svårare att läsa.
// En logaritmisk skalning med basen 20 (1, 20, 400, 8000...)
// kommer att sprida de plottade punkterna, vilket gör att vi lättare kan läsa deras värden på diagrammet.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
