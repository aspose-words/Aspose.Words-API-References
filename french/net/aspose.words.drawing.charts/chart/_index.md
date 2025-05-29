---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words pour .NET
description: Exploitez de puissantes propriétés de forme de graphique avec la classe Aspose.Words.Drawing.Charts.Chart. Améliorez vos documents grâce à une représentation visuelle dynamique des données.
type: docs
weight: 880
url: /fr/net/aspose.words.drawing.charts/chart/
---
## Chart class

Donne accès aux propriétés de forme du graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public class Chart
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Obtient une collection de tous les axes de ce graphique. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Donne accès aux propriétés de l'axe X principal du graphique. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Donne accès aux propriétés de l'axe Y principal du graphique. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Donne accès aux propriétés de l'axe Z du graphique. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | Donne accès aux propriétés d'un tableau de données de ce graphique. Le tableau de données peut être affiché à l'aide de[`Show`](../chartdatatable/show/) propriété. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | Donne accès au remplissage et au formatage des lignes du graphique. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Donne accès aux propriétés de la légende du graphique. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Donne accès à la collection de séries. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | Donne accès à une collection de groupes de séries de ce graphique. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Obtient le chemin et le nom d'un fichier xls/xlsx auquel ce graphique est lié. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | Obtient ou définit le style du graphique. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Donne accès aux propriétés du titre du graphique. |

## Exemples

Montre comment insérer un graphique et définir un titre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une forme de graphique avec un générateur de documents et obtenez son graphique.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Utilisez la propriété « Titre » pour donner un titre à notre graphique, qui apparaît en haut au centre de la zone du graphique.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

 // Définissez la propriété « Afficher » sur « true » pour rendre le titre visible.
title.Show = true;

// Définissez la propriété « Overlay » sur « true » Donnez plus d'espace aux autres éléments du graphique en leur permettant de chevaucher le titre
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
