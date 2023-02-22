---
title: AxisScaling.LogBase
second_title: Aspose.Words för .NET API Referens
description: AxisScaling fast egendom. Hämtar eller ställer in den logaritmiska basen för en logaritmisk axel.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

Hämtar eller ställer in den logaritmiska basen för en logaritmisk axel.

```csharp
public double LogBase { get; set; }
```

### Anmärkningar

Egenskapen stöds inte av MS Office 2016 nya diagram.

Giltigt intervall för ett flyttalsvärde är större än eller lika med 2 och mindre än eller lika med 1000. Egenskapen har effekt endast om[`Type`](../type/) är inställd på Logarithmic.

Om du ställer in den här egenskapen ställer du in[`Type`](../type/) egendom tillLogarithmic .

### Exempel

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

* class [AxisScaling](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../axisscaling/)
* hopsättning [Aspose.Words](../../../)


