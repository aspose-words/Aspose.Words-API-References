---
title: ChartSeries.ClearValues
linktitle: ClearValues
articleTitle: ClearValues
second_title: Aspose.Words für .NET
description: Entdecken Sie ChartSeries ClearValues. Entfernen Sie mühelos Datenwerte und behalten Sie dabei die Formatierung und Beschriftungen Ihres Diagramms bei – für ein klareres, professionelleres Erscheinungsbild.
type: docs
weight: 180
url: /de/net/aspose.words.drawing.charts/chartseries/clearvalues/
---
## ChartSeries.ClearValues method

Entfernt alle Datenwerte aus der Diagrammreihe, wobei das Format der Datenpunkte und Datenbeschriftungen erhalten bleibt.

```csharp
public void ClearValues()
```

## Beispiele

Zeigt, wie Diagrammreihen mit Daten gefüllt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// X- und Y-Werte der ersten Reihe löschen.
series1.ClearValues();

// Fülle die Reihe mit Daten.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// X- und Y-Werte der zweiten Reihe löschen.
series2.Clear();

// Fülle die Reihe mit Daten.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Siehe auch

* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
