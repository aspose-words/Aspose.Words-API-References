---
title: BubbleSizeCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FormatCode de BubbleSizeCollection pour personnaliser facilement la taille des bulles. Améliorez la visualisation de vos données grâce à des options de formatage personnalisées.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/bubblesizecollection/formatcode/
---
## BubbleSizeCollection.FormatCode property

Obtient ou définit le code de format appliqué aux tailles de bulles.

```csharp
public string FormatCode { get; set; }
```

## Remarques

Le formatage des nombres est utilisé pour modifier la façon dont les valeurs apparaissent dans le graphique. Exemples de formats de nombres :

Numéro - "#,##0.00"

Devise - "\"$\"#,##0.00"

Heure - « [$-x-systime]h:mm:ss AM/PM »

Date - « j/mm/aaaa »

Pourcentage - « 0,00 % »

Fraction - "# ?/?"

Scientifique - « 0,00E+00 »

Comptabilité - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Personnalisé avec couleur - "[Rouge]-#,##0.0"

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

* class [BubbleSizeCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
