---
title: ChartYValue.FromDouble
linktitle: FromDouble
articleTitle: FromDouble
second_title: Aspose.Words pour .NET
description: ChartYValue FromDouble méthode. Crée unChartYValue exemple duDouble tapez en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartyvalue/fromdouble/
---
## ChartYValue.FromDouble method

Crée un[`ChartYValue`](../) exemple duDouble tapez.

```csharp
public static ChartYValue FromDouble(double value)
```

## Exemples

Montre comment remplir des séries de graphiques avec des données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Efface les valeurs X et Y de la première série.
series1.ClearValues();

// Remplit la série avec des données.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9), ChartYValue.FromDouble(17));

ChartSeries series2 = chart.Series[1];

// Efface les valeurs X et Y de la deuxième série.
series2.ClearValues();

// Remplit la série avec des données.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* class [ChartYValue](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
