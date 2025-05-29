---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.ChartAxisCollection, votre solution de référence pour gérer efficacement les axes des graphiques et améliorer la visualisation des données de votre document.
type: docs
weight: 900
url: /fr/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Représente une collection d'axes de graphique.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Obtient le nombre d'axes dans cette collection. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Obtient l'axe à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Renvoie un objet énumérateur. |

## Exemples

Montre comment travailler avec la collection d'axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Masquer les principales lignes de la grille sur les axes Y primaire et secondaire.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Voir également

* class [ChartAxis](../chartaxis/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
