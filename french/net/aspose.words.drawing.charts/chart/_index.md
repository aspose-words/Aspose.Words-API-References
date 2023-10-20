---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.Chart classe. Donne accès aux propriétés de la forme du graphique en C#.
type: docs
weight: 620
url: /fr/net/aspose.words.drawing.charts/chart/
---
## Chart class

Donne accès aux propriétés de la forme du graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class Chart
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Obtient une collection de tous les axes de ce graphique. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Donne accès aux propriétés de l'axe X du graphique. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Donne accès aux propriétés de l'axe Y du graphique. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Donne accès aux propriétés de l'axe Z du graphique. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Permet d'accéder aux propriétés de la légende du graphique. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Donne accès à la collection de séries. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Obtient le chemin et le nom d'un fichier xls/xlsx auquel ce graphique est lié. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Donne accès aux propriétés du titre du graphique. |

## Exemples

Montre comment insérer un graphique et définir un titre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une forme de graphique avec un générateur de documents et récupère son graphique.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Utilisez la propriété "Titre" pour donner un titre à notre graphique, qui apparaît en haut au centre de la zone du graphique.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Définissez la propriété "Show" sur "true" pour rendre le titre visible.
title.Show = true;

// Définissez la propriété "Overlay" sur "true". Donnez plus d'espace aux autres éléments du graphique en leur permettant de chevaucher le titre.
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
