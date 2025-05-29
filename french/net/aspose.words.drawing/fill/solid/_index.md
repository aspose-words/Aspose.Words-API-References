---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Fill Solid pour obtenir un remplissage de couleur uniforme, améliorant ainsi l'attrait visuel et l'uniformité de votre conception sans effort.
type: docs
weight: 260
url: /fr/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Définit le remplissage sur une couleur uniforme.

```csharp
public void Solid()
```

## Remarques

Utilisez cette méthode pour reconvertir n'importe quel remplissage en remplissage solide.

## Exemples

Montre comment reconvertir n'importe quel remplissage en remplissage solide.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Obtenir l'objet Fill pour la police de la première exécution.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Vérifiez les propriétés de remplissage de la police.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Changez le type de remplissage en Solide avec une couleur verte uniforme.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Définit le remplissage sur une couleur uniforme spécifiée.

```csharp
public void Solid(Color color)
```

## Remarques

Utilisez cette méthode pour reconvertir n'importe quel remplissage en remplissage solide.

## Exemples

Montre comment utiliser le formatage des graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Supprimer les séries générées par défaut.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Formater l'arrière-plan du graphique.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Masquer les étiquettes des graduations des axes.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Formater le titre du graphique.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formater le titre de l'axe.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formater la légende.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
