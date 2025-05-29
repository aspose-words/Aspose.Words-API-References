---
title: ChartFormat.Stroke
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartFormat Stroke para mejorar el estilo de línea en sus gráficos, garantizando presentaciones profesionales y visualmente atractivas.
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/chartformat/stroke/
---
## ChartFormat.Stroke property

Obtiene el formato de línea para el elemento del gráfico principal.

```csharp
public Stroke Stroke { get; }
```

## Ejemplos

Muestra cómo establecer el formato del marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

//Eliminar serie generada por defecto.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Establecer el formato del marcador.
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

### Ver también

* class [Stroke](../../../aspose.words.drawing/stroke/)
* class [ChartFormat](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
