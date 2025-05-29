---
title: DocumentBuilder.InsertChart
linktitle: InsertChart
articleTitle: InsertChart
second_title: Aspose.Words pour .NET
description: Améliorez vos documents sans effort grâce à la méthode InsertChart de DocumentBuilder. Ajoutez et redimensionnez facilement des objets graphiques pour des présentations percutantes.
type: docs
weight: 280
url: /fr/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double*) {#insertchart_2}

Insère un objet graphique dans le document et le met à l'échelle à la taille spécifiée.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| chartType | ChartType | Le type de graphique à insérer dans le document. |
| width | Double | Largeur de l'image en points. Cette valeur peut être négative ou nulle pour une échelle de 100 %. |
| height | Double | Hauteur de l'image en points. Cette valeur peut être négative ou nulle pour une échelle de 100 %. |

### Return_Value

Le nœud d’image qui vient d’être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide de [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

## Exemples

Montre comment insérer un graphique à secteurs dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, ConvertUtil.PixelToPoint(300), 
    ConvertUtil.PixelToPoint(300)).Chart;
chart.Series.Clear();
chart.Series.Add("My fruit",
    new[] { "Apples", "Bananas", "Cherries" },
    new[] { 1.3, 2.2, 1.5 });

doc.Save(ArtifactsDir + "DocumentBuilder.InsertPieChart.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_3}

Insère un objet graphique dans le document et le met à l'échelle à la taille spécifiée.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height, ChartStyle chartStyle)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| chartType | ChartType | Le type de graphique à insérer dans le document. |
| width | Double | Largeur de l'image en points. Cette valeur peut être négative ou nulle pour une échelle de 100 %. |
| height | Double | Hauteur de l'image en points. Cette valeur peut être négative ou nulle pour une échelle de 100 %. |
| chartStyle | ChartStyle | Le style du graphique inséré. |

### Return_Value

Le nœud d’image qui vient d’être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide de [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertchart}

Insère un objet graphique dans le document et le met à l'échelle à la taille spécifiée.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| chartType | ChartType | Le type de graphique à insérer dans le document. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance par rapport à l'image est mesurée. |
| left | Double | Distance en points de l'origine au côté gauche de l'image. |
| vertPos | RelativeVerticalPosition | Spécifie d'où la distance par rapport à l'image est mesurée. |
| top | Double | Distance en points de l'origine au côté supérieur de l'image. |
| width | Double | Largeur de l'image en points. Cette valeur peut être négative ou nulle pour une échelle de 100 %. |
| height | Double | Hauteur de l'image en points. Cette valeur peut être négative ou nulle pour une échelle de 100 %. |
| wrapType | WrapType | Spécifie comment envelopper le texte autour de l'image. |

### Return_Value

Le nœud d’image qui vient d’être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide de [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

## Exemples

Montre comment spécifier la position et l'habillage lors de l'insertion d'un graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertChart(ChartType.Pie, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
    100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertedChartRelativePosition.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/), [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_1}

Insère un objet graphique dans le document et le met à l'échelle à la taille spécifiée.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType, 
    ChartStyle chartStyle)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| chartType | ChartType | Le type de graphique à insérer dans le document. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance par rapport à l'image est mesurée. |
| left | Double | Distance en points de l'origine au côté gauche de l'image. |
| vertPos | RelativeVerticalPosition | Spécifie d'où la distance par rapport à l'image est mesurée. |
| top | Double | Distance en points de l'origine au côté supérieur de l'image. |
| width | Double | Largeur de l'image en points. Cette valeur peut être négative ou nulle pour une échelle de 100 %. |
| height | Double | Hauteur de l'image en points. Cette valeur peut être négative ou nulle pour une échelle de 100 %. |
| wrapType | WrapType | Spécifie comment envelopper le texte autour de l'image. |
| chartStyle | ChartStyle | Le style du graphique inséré. |

### Return_Value

Le nœud d’image qui vient d’être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide de [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
