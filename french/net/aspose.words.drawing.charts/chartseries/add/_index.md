---
title: ChartSeries.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Découvrez la méthode ChartSeries Add pour intégrer facilement les valeurs X à vos graphiques. Améliorez la visualisation des données grâce à la prise en charge des valeurs Y et des tailles de bulles.
type: docs
weight: 160
url: /fr/net/aspose.words.drawing.charts/chartseries/add/
---
## Add(*[ChartXValue](../../chartxvalue/)*) {#add}

Ajoute la valeur X spécifiée à la série de graphiques. Si la série prend en charge les valeurs Y et les tailles de bulle, elles seront vides pour la valeur X.

```csharp
public void Add(ChartXValue xValue)
```

## Exemples

Montre comment remplir des séries de graphiques avec des données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Effacer les valeurs X et Y de la première série.
series1.ClearValues();

// Remplir la série avec des données.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Effacer les valeurs X et Y de la deuxième série.
series2.Clear();

// Remplir la série avec des données.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#add_1}

Ajoute les valeurs X et Y spécifiées à la série de graphiques.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
```

## Exemples

Montre comment ajouter/supprimer des valeurs de données de graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Supprimez la première valeur des deux séries.
department1Series.Remove(0);
department2Series.Remove(0);

// Ajouter de nouvelles valeurs aux deux séries.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

Montre comment remplir des séries de graphiques avec des données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Effacer les valeurs X et Y de la première série.
series1.ClearValues();

// Remplir la série avec des données.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Effacer les valeurs X et Y de la deuxième série.
series2.Clear();

// Remplir la série avec des données.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#add_2}

Ajoute la valeur X, la valeur Y et la taille de la bulle spécifiées à la série de graphiques.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Exemples

Montre comment remplir des séries de graphiques avec des données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Effacer les valeurs X et Y de la première série.
series1.ClearValues();

// Remplir la série avec des données.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Effacer les valeurs X et Y de la deuxième série.
series2.Clear();

// Remplir la série avec des données.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
