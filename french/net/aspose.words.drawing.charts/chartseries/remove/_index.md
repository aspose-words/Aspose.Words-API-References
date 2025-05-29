---
title: ChartSeries.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: Supprimez facilement les valeurs X, Y et la taille des bulles de vos séries de graphiques grâce à la méthode ChartSeries Remove. Simplifiez la visualisation de vos données dès aujourd'hui !
type: docs
weight: 210
url: /fr/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

Supprime la valeur X, la valeur Y et la taille de la bulle, si elles sont prises en charge, de la série de graphiques à l'index spécifié. Le point de données et l'étiquette de données correspondants sont également supprimés.

```csharp
public void Remove(int index)
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

// Supprimez la première valeur des deux séries.
department1Series.Remove(0);
department2Series.Remove(0);

// Ajouter de nouvelles valeurs aux deux séries.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Voir également

* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
