---
title: ChartSeries.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words pour .NET
description: Améliorez facilement vos graphiques grâce à la méthode d'insertion de ChartSeries. Insérez des valeurs X à n'importe quel index et optimisez ainsi la visualisation de vos données en toute simplicité !
type: docs
weight: 200
url: /fr/net/aspose.words.drawing.charts/chartseries/insert/
---
## Insert(*int, [ChartXValue](../../chartxvalue/)*) {#insert}

Insère la valeur X spécifiée dans la série de graphiques à l'index spécifié. Si la série prend en charge les valeurs Y et les tailles de bulle, elles seront vides pour la valeur X.

```csharp
public void Insert(int index, ChartXValue xValue)
```

## Remarques

Le point de données correspondant, avec le formatage par défaut, sera inséré dans la collection de points de données. De plus, si des étiquettes de données sont affichées, l'étiquette correspondante avec le formatage par défaut sera également insérée.

## Exemples

Montre comment insérer des données dans une série de graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Effacer les valeurs X et Y de la première série.
series1.ClearValues();
// Remplir la série avec des données.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#insert_1}

Insère les valeurs X et Y spécifiées dans la série de graphiques à l'index spécifié.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue)
```

## Remarques

Le point de données correspondant, avec le formatage par défaut, sera inséré dans la collection de points de données. De plus, si des étiquettes de données sont affichées, l'étiquette correspondante avec le formatage par défaut sera également insérée.

## Exemples

Montre comment insérer des données dans une série de graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Effacer les valeurs X et Y de la première série.
series1.ClearValues();
// Remplir la série avec des données.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#insert_2}

Insère la valeur X, la valeur Y et la taille de bulle spécifiées dans la série de graphiques à l'index spécifié.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Remarques

Le point de données correspondant, avec le formatage par défaut, sera inséré dans la collection de points de données. De plus, si des étiquettes de données sont affichées, l'étiquette correspondante avec le formatage par défaut sera également insérée.

## Exemples

Montre comment insérer des données dans une série de graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Effacer les valeurs X et Y de la première série.
series1.ClearValues();
// Remplir la série avec des données.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
