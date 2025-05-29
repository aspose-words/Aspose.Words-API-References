---
title: ChartMultilevelValue Class
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.ChartMultilevelValue pour gérer efficacement les données multiniveaux dans vos graphiques, améliorant ainsi vos capacités de visualisation des données.
type: docs
weight: 1050
url: /fr/net/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class

Représente une valeur pour les graphiques qui affichent des données à plusieurs niveaux.

```csharp
public class ChartMultilevelValue
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor)(*string*) | Initialise une nouvelle instance de cette classe qui représente une valeur à un seul niveau. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_1)(*string, string*) | Initialise une nouvelle instance de cette classe qui représente une valeur à deux niveaux. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_2)(*string, string, string*) | Initialise une nouvelle instance de cette classe qui représente une valeur à trois niveaux. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Level1](../../aspose.words.drawing.charts/chartmultilevelvalue/level1/) { get; } | Obtient le nom du niveau supérieur du graphique auquel cette valeur fait référence. |
| [Level2](../../aspose.words.drawing.charts/chartmultilevelvalue/level2/) { get; } | Obtient le nom du niveau intermédiaire du graphique auquel cette valeur fait référence. |
| [Level3](../../aspose.words.drawing.charts/chartmultilevelvalue/level3/) { get; } | Obtient le nom du niveau inférieur du graphique auquel cette valeur fait référence. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/chartmultilevelvalue/equals/)(*object*) | Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet de données multiniveau actuel. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartmultilevelvalue/gethashcode/)() | Obtient un code de hachage pour l'objet de données multiniveau actuel. |

## Exemples

Montre comment créer un graphique arborescent.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique Treemap.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une série.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// Afficher les étiquettes de données.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
