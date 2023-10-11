---
title: Stroke.Transparency
second_title: Référence de l'API Aspose.Words pour .NET
description: Stroke propriété. Obtient ou définit une valeur comprise entre 00 opaque et 10 clair représentant le degré de transparence du trait.
type: docs
weight: 200
url: /fr/net/aspose.words.drawing/stroke/transparency/
---
## Stroke.Transparency property

Obtient ou définit une valeur comprise entre 0,0 (opaque) et 1,0 (clair) représentant le degré de transparence du trait.

```csharp
public double Transparency { get; set; }
```

### Remarques

La valeur par défaut est 0.

### Exemples

Montrez comment définir le formatage des marqueurs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Supprime la série générée par défaut.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Définit le formatage du marqueur.
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

### Voir également

* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../stroke/)
* Assemblée [Aspose.Words](../../../)


