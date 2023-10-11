---
title: ChartNumberFormat.FormatCode
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartNumberFormat propriété. Obtient ou définit le code de format appliqué à une étiquette de données.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

Obtient ou définit le code de format appliqué à une étiquette de données.

```csharp
public string FormatCode { get; set; }
```

### Remarques

Le formatage des nombres est utilisé pour modifier la façon dont une valeur apparaît dans l'étiquette de données et peut être utilisé de manière très créative. Les exemples de formats de nombres :

Numéro - "#,##0.00"

Devise - "\"$\"#,##0.00"

Heure - "[$-x-systime]h:mm:ss AM/PM"

Date - "j/mm/aaaa"

Pourcentage - "0,00%"

Fraction - "# ?/?"

Scientifique - "0.00E+00"

Texte - "@"

Comptabilité - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_ -;_-@_-"

Personnalisé avec couleur - "[Rouge]-#,##0.0"

### Exemples

Montre comment définir le formatage des valeurs du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Efface la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Ajout d'une série personnalisée au graphique avec des catégories pour l'axe X,
 // et de grandes valeurs numériques respectives pour l'axe Y.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Définit le format numérique des étiquettes de graduation de l'axe Y pour ne pas regrouper les chiffres avec des virgules.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Cet indicateur peut remplacer la valeur ci-dessus et extraire le format numérique de la cellule source.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

Montre comment activer et configurer les étiquettes de données pour une série de graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez un graphique linéaire, puis effacez sa série de données de démonstration pour commencer avec un graphique propre,
// puis définissez un titre.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Insère une série de graphiques personnalisés avec des mois comme catégories pour l'axe X,
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
* espace de noms [Aspose.Words.Drawing.Charts](../../chartnumberformat/)
* Assemblée [Aspose.Words](../../../)


