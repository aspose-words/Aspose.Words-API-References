---
title: ChartSeries.HasDataLabels
linktitle: HasDataLabels
articleTitle: HasDataLabels
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeries HasDataLabels pour gérer facilement la visibilité des étiquettes de données pour votre série, améliorant ainsi votre expérience de visualisation des données.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.charts/chartseries/hasdatalabels/
---
## ChartSeries.HasDataLabels property

Obtient ou définit un indicateur indiquant si les étiquettes de données sont affichées pour la série.

```csharp
public bool HasDataLabels { get; set; }
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

* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
