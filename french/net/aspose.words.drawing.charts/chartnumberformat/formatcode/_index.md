---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la propriété FormatCode de ChartNumberFormat pour personnaliser les formats d'étiquettes de données pour des informations plus claires et une présentation des données améliorée.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

Obtient ou définit le code de format appliqué à une étiquette de données.

```csharp
public string FormatCode { get; set; }
```

## Remarques

Le formatage des nombres est utilisé pour modifier la façon dont une valeur apparaît dans l'étiquette de données et peut être utilisé de manière très créative. Exemples de formats de nombres :

Numéro - "#,##0.00"

Devise - "\"$\"#,##0.00"

Heure - « [$-x-systime]h:mm:ss AM/PM »

Date - « j/mm/aaaa »

Pourcentage - « 0,00 % »

Fraction - "# ?/?"

Scientifique - « 0,00E+00 »

Texte - "@"

Comptabilité - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Personnalisé avec couleur - "[Rouge]-#,##0.0"

## Exemples

Montre comment définir la mise en forme des valeurs du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Effacez la série de données de démonstration du graphique pour démarrer avec un graphique propre.
chart.Series.Clear();

// Ajouter une série personnalisée au graphique avec des catégories pour l'axe des X,
 // et de grandes valeurs numériques respectives pour l'axe Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Définissez le format numérique des étiquettes de graduation de l'axe Y pour ne pas regrouper les chiffres avec des virgules.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Cet indicateur peut remplacer la valeur ci-dessus et dessiner le format numérique à partir de la cellule source.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

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

* class [ChartNumberFormat](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
