---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartAxis NumberFormat pour personnaliser sans effort les formats numériques de votre graphique avec l'objet ChartNumberFormat pour une visualisation améliorée des données.
type: docs
weight: 200
url: /fr/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Renvoie un[`ChartNumberFormat`](../../chartnumberformat/) objet permettant de définir des formats de nombres pour l'axe.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

### Voir également

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
