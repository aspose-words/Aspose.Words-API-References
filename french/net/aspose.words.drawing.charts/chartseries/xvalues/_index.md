---
title: ChartSeries.XValues
linktitle: XValues
articleTitle: XValues
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeries XValues pour accéder à une puissante collection de valeurs X, améliorant ainsi la visualisation et l'analyse de vos données.
type: docs
weight: 140
url: /fr/net/aspose.words.drawing.charts/chartseries/xvalues/
---
## ChartSeries.XValues property

Obtient une collection de valeurs X pour cette série de graphiques.

```csharp
public ChartXValueCollection XValues { get; }
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

* class [ChartXValueCollection](../../chartxvaluecollection/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
