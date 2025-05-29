---
title: ChartSeries.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Diagramme mühelos mit der ChartSeries-Einfügemethode. Fügen Sie X-Werte an jedem Index ein und optimieren Sie so Ihre Datenvisualisierung im Handumdrehen!
type: docs
weight: 200
url: /de/net/aspose.words.drawing.charts/chartseries/insert/
---
## Insert(*int, [ChartXValue](../../chartxvalue/)*) {#insert}

Fügt den angegebenen X-Wert am angegebenen Index in die Diagrammreihe ein. Wenn die Reihe Y-Werte und Blasengrößen unterstützt, sind diese für den X-Wert leer.

```csharp
public void Insert(int index, ChartXValue xValue)
```

## Bemerkungen

Der entsprechende Datenpunkt mit Standardformatierung wird in die Datenpunktsammlung eingefügt. Und Wenn Datenbeschriftungen angezeigt werden, wird auch die entsprechende Datenbeschriftung mit Standardformatierung eingefügt.

## Beispiele

Zeigt, wie Daten in eine Diagrammreihe eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// X- und Y-Werte der ersten Reihe löschen.
series1.ClearValues();
// Fülle die Reihe mit Daten.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Siehe auch

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#insert_1}

Fügt die angegebenen X- und Y-Werte am angegebenen Index in die Diagrammreihe ein.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue)
```

## Bemerkungen

Der entsprechende Datenpunkt mit Standardformatierung wird in die Datenpunktsammlung eingefügt. Und Wenn Datenbeschriftungen angezeigt werden, wird auch die entsprechende Datenbeschriftung mit Standardformatierung eingefügt.

## Beispiele

Zeigt, wie Daten in eine Diagrammreihe eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// X- und Y-Werte der ersten Reihe löschen.
series1.ClearValues();
// Fülle die Reihe mit Daten.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Siehe auch

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#insert_2}

Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße am angegebenen Index in die Diagrammreihe ein.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Bemerkungen

Der entsprechende Datenpunkt mit Standardformatierung wird in die Datenpunktsammlung eingefügt. Und Wenn Datenbeschriftungen angezeigt werden, wird auch die entsprechende Datenbeschriftung mit Standardformatierung eingefügt.

## Beispiele

Zeigt, wie Daten in eine Diagrammreihe eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// X- und Y-Werte der ersten Reihe löschen.
series1.ClearValues();
// Fülle die Reihe mit Daten.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Siehe auch

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
