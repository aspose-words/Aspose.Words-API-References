---
title: ChartAxis.NumberFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartAxis propriété. Renvoie unChartNumberFormat objet qui permet de définir des formats numériques pour laxe.
type: docs
weight: 190
url: /fr/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Renvoie un[`ChartNumberFormat`](../../chartnumberformat/) objet qui permet de définir des formats numériques pour l'axe.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

### Voir également

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartaxis/)
* Assemblée [Aspose.Words](../../../)


