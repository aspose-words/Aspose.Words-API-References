---
title: Chart.Title
second_title: Référence de l'API Aspose.Words pour .NET
description: Chart propriété. Donne accès aux propriétés du titre du graphique.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

Donne accès aux propriétés du titre du graphique.

```csharp
public ChartTitle Title { get; }
```

### Exemples

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chart/)
* Assemblée [Aspose.Words](../../../)


