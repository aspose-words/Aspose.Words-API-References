---
title: ChartYValue.FromDouble
linktitle: FromDouble
articleTitle: FromDouble
second_title: Aspose.Words für .NET
description: ChartYValue FromDouble methode. Erstellt eineChartYValue Instanz derDouble Typ in C#.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartyvalue/fromdouble/
---
## ChartYValue.FromDouble method

Erstellt eine[`ChartYValue`](../) Instanz derDouble Typ.

```csharp
public static ChartYValue FromDouble(double value)
```

## Beispiele

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

* class [ChartYValue](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
