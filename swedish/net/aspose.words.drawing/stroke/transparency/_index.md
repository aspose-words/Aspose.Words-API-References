---
title: Stroke.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words för .NET
description: Justera egenskapen Linjetransparens för att kontrollera opaciteten från 0,0 (ogenomskinlig) till 1,0 (klar), vilket förbättrar designens visuella effekt.
type: docs
weight: 240
url: /sv/net/aspose.words.drawing/stroke/transparency/
---
## Stroke.Transparency property

Hämtar eller ställer in ett värde mellan 0,0 (ogenomskinlig) och 1,0 (klar) som representerar graden av genomskinlighet för linjen.

```csharp
public double Transparency { get; set; }
```

## Anmärkningar

Standardvärdet är 0.

## Exempel

Visa hur man ställer in markörformatering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Radera standardgenererad serie.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Ange markörformatering.
series.Marker.Size = 40;
series.Marker.Symbol = MarkerSymbol.Square;
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Marker.Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[0].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[0].Marker.Format.Stroke.BackColor = Color.Red;
dataPoints[1].Marker.Format.Fill.PresetTextured(PresetTexture.WaterDroplets);
dataPoints[1].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[1].Marker.Format.Stroke.Visible = false;
dataPoints[2].Marker.Format.Fill.PresetTextured(PresetTexture.GreenMarble);
dataPoints[2].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Fill.PresetTextured(PresetTexture.Oak);
dataPoints[3].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Stroke.Transparency = 0.5;

doc.Save(ArtifactsDir + "Charts.MarkerFormatting.docx");
```

### Se även

* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
