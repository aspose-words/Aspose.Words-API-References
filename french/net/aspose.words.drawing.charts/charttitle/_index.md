---
title: Class ChartTitle
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartTitle classe. Fournit un accès aux propriétés du titre du graphique.
type: docs
weight: 750
url: /fr/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Fournit un accès aux propriétés du titre du graphique.

```csharp
public class ChartTitle
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Détermine si d'autres éléments du graphique doivent être autorisés à chevaucher le titre. Par défaut, la superposition est fausse. |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Détermine si le titre doit être affiché pour ce graphique. La valeur par défaut est true. |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Obtient ou définit le texte du titre du graphique. Si une valeur nulle ou vide est spécifiée, le titre généré automatiquement sera affiché. |

### Exemples

Montre comment insérer un graphique et définir un titre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une forme de graphique avec un générateur de document et récupère son graphique.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Utilisez la propriété "Titre" pour donner à notre graphique un titre, qui apparaît en haut au centre de la zone du graphique.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Définissez la propriété "Show" sur "true" pour rendre le titre visible.
title.Show = true;

// Définit la propriété "Overlay" sur "true" Donne plus de place aux autres éléments du graphique en leur permettant de chevaucher le titre
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)


