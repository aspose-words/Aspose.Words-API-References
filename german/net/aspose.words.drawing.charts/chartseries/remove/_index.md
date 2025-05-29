---
title: ChartSeries.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos X-Werte, Y-Werte und Blasengrößen aus Ihren Diagrammreihen mit der Methode „ChartSeries Remove“. Optimieren Sie Ihre Datenvisualisierung noch heute!
type: docs
weight: 210
url: /de/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

Entfernt den X-Wert, den Y-Wert und die Blasengröße (sofern unterstützt) aus der Diagrammreihe am angegebenen Index. Der entsprechende Datenpunkt und die Datenbeschriftung werden ebenfalls entfernt.

```csharp
public void Remove(int index)
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

// Entfernen Sie den ersten Wert in beiden Reihen.
department1Series.Remove(0);
department2Series.Remove(0);

// Fügen Sie beiden Reihen neue Werte hinzu.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### Siehe auch

* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
