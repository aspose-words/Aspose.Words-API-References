---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartDataLabelCollection NumberFormat pour personnaliser facilement les formats d'étiquettes de données pour l'ensemble de votre série, améliorant ainsi la clarté et la présentation.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Obtient un[`ChartNumberFormat`](../../chartnumberformat/) instance permettant de définir le format numérique des étiquettes de données de la série entière.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
