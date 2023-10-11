---
title: ChartTitle.Show
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartTitle propriété. Détermine si le titre doit être affiché pour ce graphique. La valeur par défaut estvrai .
type: docs
weight: 30
url: /fr/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

Détermine si le titre doit être affiché pour ce graphique. La valeur par défaut est`vrai` .

```csharp
public bool Show { get; set; }
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

* class [ChartTitle](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../charttitle/)
* Assemblée [Aspose.Words](../../../)


