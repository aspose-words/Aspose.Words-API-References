---
title: ChartSeries.YValues
linktitle: YValues
articleTitle: YValues
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeries YValues pour accéder à une puissante collection de valeurs Y, améliorant ainsi vos capacités de visualisation et d'analyse de données.
type: docs
weight: 150
url: /fr/net/aspose.words.drawing.charts/chartseries/yvalues/
---
## ChartSeries.YValues property

Obtient une collection de valeurs Y pour cette série de graphiques.

```csharp
public ChartYValueCollection YValues { get; }
```

## Exemples

Montre comment travailler avec le code de format des données du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique à bulles.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Supprimer la série générée par défaut.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Afficher les étiquettes de données.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Définir les codes de format de données.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Voir également

* class [ChartYValueCollection](../../chartyvaluecollection/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
