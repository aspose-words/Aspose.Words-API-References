---
title: AxisScaleType Enum
linktitle: AxisScaleType
articleTitle: AxisScaleType
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Drawing.Charts.AxisScaleType, som definierar mångsidiga axelskalningstyper för att förbättra din diagramupplevelse.
type: docs
weight: 810
url: /sv/net/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enumeration

Anger möjliga skaltyper för en axel.

```csharp
public enum AxisScaleType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Linear | `0` | Linjär skalning. |
| Logarithmic | `1` | Logaritmisk skalning. |

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
// visar jämnt ökande värden som täcker vårt X-värdeintervall (0, 1, 2, 3...).
// En linjär axel är inte idealisk för våra Y-värden
// eftersom punkterna med de mindre Y-värdena blir svårare att läsa.
// En logaritmisk skalning med basen 20 (1, 20, 400, 8000...)
// kommer att sprida ut de plottade punkterna, vilket gör att vi lättare kan läsa deras värden i diagrammet.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
