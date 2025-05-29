---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartNumberFormat pour une mise en forme numérique avancée dans les graphiques. Améliorez l'attrait visuel de votre document !
type: docs
weight: 1060
url: /fr/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

Représente le formatage numérique de l'élément parent.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public class ChartNumberFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | Obtient ou définit le code de format appliqué à une étiquette de données. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | Spécifie si le code de format est lié à une cellule source. La valeur par défaut est vrai. |

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
