---
title: Class Chart
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.Chart classe. Fournit un accès aux propriétés de la forme du graphique.
type: docs
weight: 600
url: /fr/net/aspose.words.drawing.charts/chart/
---
## Chart class

Fournit un accès aux propriétés de la forme du graphique.

```csharp
public class Chart
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Permet d'accéder aux propriétés de l'axe X du graphique. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Permet d'accéder aux propriétés de l'axe Y du graphique. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Permet d'accéder aux propriétés de l'axe Z du graphique. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Fournit l'accès aux propriétés de la légende du graphique. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Fournit l'accès à la collection de séries. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Obtient le chemin et le nom d'un fichier xls/xlsx auquel ce graphique est lié. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Fournit un accès aux propriétés du titre du graphique. |

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


