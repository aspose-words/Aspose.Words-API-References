---
title: ChartDataLabelCollection.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words pour .NET
description: Accédez et personnalisez la mise en forme de police de l'ensemble des étiquettes de données de votre série avec la propriété Police ChartDataLabelCollection pour une visualisation améliorée des données.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

Donne accès au formatage des polices des étiquettes de données de toute la série.

```csharp
public Font Font { get; }
```

## Remarques

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant le [`Font`](../../chartdatalabel/font/) propriété.

## Exemples

Montre comment activer et configurer les étiquettes de données pour une série de graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez un graphique linéaire, puis effacez sa série de données de démonstration pour démarrer avec un graphique propre,
// puis définissez un titre.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Insérer une série de graphiques personnalisés avec les mois comme catégories pour l'axe des X,
// et les montants décimaux respectifs pour l'axe Y.
ChartSeries series = chart.Series.Add("Revenue",
    new[] { "January", "February", "March" },
    new[] { 25.611d, 21.439d, 33.750d });

// Activez les étiquettes de données, puis appliquez un format numérique personnalisé pour les valeurs affichées dans les étiquettes de données.
// Ce format traitera les valeurs décimales affichées comme des millions de dollars américains.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### Voir également

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
