---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: Aspose.Words pour .NET
description: ChartXValue FromString méthode. Crée unChartXValue exemple duString tapez en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Crée un[`ChartXValue`](../) exemple duString tapez.

```csharp
public static ChartXValue FromString(string value)
```

## Exemples

Montre comment ajouter/supprimer des valeurs de données de graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Supprime la première valeur des deux séries.
department1Series.Remove(0);
department2Series.Remove(0);

// Ajoute de nouvelles valeurs aux deux séries.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Voir également

* class [ChartXValue](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
