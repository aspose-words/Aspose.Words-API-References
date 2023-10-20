---
title: ChartSeries.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: ChartSeries Add methode. Fügt den angegebenen XWert zur Diagrammreihe hinzu. Wenn die Reihe YWerte und Blasengrößen unterstützt sind diese für den XWert leer in C#.
type: docs
weight: 160
url: /de/net/aspose.words.drawing.charts/chartseries/add/
---
## Add(*[ChartXValue](../../chartxvalue/)*) {#add}

Fügt den angegebenen X-Wert zur Diagrammreihe hinzu. Wenn die Reihe Y-Werte und Blasengrößen unterstützt, sind diese für den X-Wert leer.

```csharp
public void Add(ChartXValue xValue)
```

### Siehe auch

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#add_1}

Fügt die angegebenen X- und Y-Werte zur Diagrammreihe hinzu.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
```

## Beispiele

Zeigt, wie Diagrammdatenwerte hinzugefügt/entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Den ersten Wert in beiden Reihen entfernen.
department1Series.Remove(0);
department2Series.Remove(0);

// Neue Werte zu beiden Reihen hinzufügen.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

Zeigt, wie Diagrammreihen mit Daten gefüllt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// X- und Y-Werte der ersten Serie löschen.
series1.ClearValues();

// Die Reihe mit Daten füllen.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9), ChartYValue.FromDouble(17));

ChartSeries series2 = chart.Series[1];

// X- und Y-Werte der zweiten Reihe löschen.
series2.ClearValues();

// Die Reihe mit Daten füllen.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Siehe auch

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#add_2}

Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße zur Diagrammreihe hinzu.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

### Siehe auch

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
