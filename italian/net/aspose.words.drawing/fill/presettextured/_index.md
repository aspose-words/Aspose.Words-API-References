---
title: Fill.PresetTextured
second_title: Aspose.Words per .NET API Reference
description: Fill metodo. Imposta il riempimento su una texture preimpostata.
type: docs
weight: 240
url: /it/net/aspose.words.drawing/fill/presettextured/
---
## Fill.PresetTextured method

Imposta il riempimento su una texture preimpostata.

```csharp
public void PresetTextured(PresetTexture presetTexture)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| presetTexture | PresetTexture | [`PresetTexture`](../../presettexture/) |

### Esempi

Mostra come impostare la formattazione del marcatore.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Elimina le serie generate predefinite.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Imposta la formattazione del marcatore.
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

### Guarda anche

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../fill/)
* assemblea [Aspose.Words](../../../)


