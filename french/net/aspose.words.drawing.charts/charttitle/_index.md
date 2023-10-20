---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartTitle classe. Donne accès aux propriétés du titre du graphique en C#.
type: docs
weight: 820
url: /fr/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Donne accès aux propriétés du titre du graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques ](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class ChartTitle
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Détermine si d'autres éléments du graphique doivent être autorisés à chevaucher le titre. Par défaut, la superposition est`FAUX` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Détermine si le titre doit être affiché pour ce graphique. La valeur par défaut est`vrai` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Obtient ou définit le texte du titre du graphique. Si`nul` ou une valeur vide est spécifiée, le titre généré automatiquement sera affiché. |

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
