---
title: ChartTitle.Overlay
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartTitle propriété. Détermine si dautres éléments du graphique doivent être autorisés à chevaucher le titre. Par défaut la superposition estFAUX .
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/charttitle/overlay/
---
## ChartTitle.Overlay property

Détermine si d'autres éléments du graphique doivent être autorisés à chevaucher le titre. Par défaut, la superposition est`FAUX` .

```csharp
public bool Overlay { get; set; }
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


