---
title: Fill.PresetTextured
second_title: Referencia de API de Aspose.Words para .NET
description: Fill método. Establece el relleno en una textura preestablecida.
type: docs
weight: 180
url: /es/net/aspose.words.drawing/fill/presettextured/
---
## Fill.PresetTextured method

Establece el relleno en una textura preestablecida.

```csharp
public void PresetTextured(PresetTexture presetTexture)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| presetTexture | PresetTexture | [`PresetTexture`](../../presettexture/) |

### Ejemplos

Muestre cómo configurar el formato de marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Elimina la serie generada por defecto.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Establecer formato de marcador.
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

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../fill/)
* asamblea [Aspose.Words](../../../)


