---
title: ChartDataPoint.Format
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartDataPoint propriété. Donne accès au formatage de remplissage et de ligne de ce point de données.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Donne accès au formatage de remplissage et de ligne de ce point de données.

```csharp
public ChartFormat Format { get; }
```

### Exemples

Montre comment définir une mise en forme individuelle pour les catégories d’un histogramme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Supprime la série générée par défaut.
chart.Series.Clear();

// Ajout d'une nouvelle série.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Définit le formatage des colonnes.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

### Voir également

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartdatapoint/)
* Assemblée [Aspose.Words](../../../)


