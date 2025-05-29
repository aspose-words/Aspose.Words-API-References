---
title: ChartSeries.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words pour .NET
description: Optimisez vos graphiques avec la méthode ChartSeries Clear ! Supprimez facilement des valeurs de données et réinitialisez la mise en forme pour un rendu plus net et plus professionnel.
type: docs
weight: 170
url: /fr/net/aspose.words.drawing.charts/chartseries/clear/
---
## ChartSeries.Clear method

Supprime toutes les valeurs de données de la série de graphiques. Le format de tous les points de données et étiquettes de données est effacé.

```csharp
public void Clear()
```

## Exemples

Montre comment remplir des séries de graphiques avec des données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Effacer les valeurs X et Y de la première série.
series1.ClearValues();

// Remplir la série avec des données.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Effacer les valeurs X et Y de la deuxième série.
series2.Clear();

// Remplir la série avec des données.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
