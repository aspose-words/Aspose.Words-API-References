---
title: ChartTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: Personnalisez facilement le titre de votre graphique ! Définissez ou obtenez la propriété Texte du titre du graphique pour une touche personnelle. Générez automatiquement les titres si nécessaire.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Obtient ou définit le texte du titre du graphique. Si`nul` ou une valeur vide est spécifiée, le titre généré automatiquement sera affiché.

```csharp
public string Text { get; set; }
```

## Remarques

Utiliser[`Show`](../show/) option si vous devez masquer le titre.

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

* class [ChartTitle](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
