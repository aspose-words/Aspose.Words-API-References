---
title: Stroke.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words para .NET
description: Ajuste la propiedad Transparencia del trazo para controlar la opacidad de 0.0 (opaco) a 1.0 (transparente), mejorando el impacto visual de su diseño.
type: docs
weight: 240
url: /es/net/aspose.words.drawing/stroke/transparency/
---
## Stroke.Transparency property

Obtiene o establece un valor entre 0,0 (opaco) y 1,0 (transparente) que representa el grado de transparencia del trazo.

```csharp
public double Transparency { get; set; }
```

## Observaciones

El valor predeterminado es 0.

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

* class [Stroke](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
