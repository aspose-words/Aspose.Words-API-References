---
title: ChartDataPoint.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété Format ChartDataPoint améliore la visualisation de vos données avec des styles de remplissage et de ligne personnalisables pour des présentations percutantes.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Fournit l'accès au remplissage et au formatage des lignes de ce point de données.

```csharp
public ChartFormat Format { get; }
```

## Exemples

Montre comment définir une mise en forme individuelle pour les catégories d'un graphique à colonnes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajout d'une nouvelle série.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Définir la mise en forme des colonnes.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

Montre comment travailler avec des points de données sur un graphique linéaire.

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Mettez en valeur les points de données du graphique en les faisant apparaître sous forme de losanges.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Lissez la ligne qui représente la première série de données.
    chart.Series[0].Smooth = true;

    // Vérifiez que les points de données de la première série n'inverseront pas leurs couleurs si la valeur est négative.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // Pour un graphique plus propre, nous pouvons effacer le format individuellement.
    dataPoint.ClearFormat();

    // Nous pouvons également supprimer une série entière de points de données à la fois.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Applique un certain nombre de points de données à une série.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### Voir également

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
