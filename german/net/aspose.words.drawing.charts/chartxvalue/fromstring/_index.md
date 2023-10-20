---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: Aspose.Words für .NET
description: ChartXValue FromString methode. Erstellt eineChartXValue Instanz derString Typ in C#.
type: docs
weight: 40
url: /de/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

Erstellt eine[`ChartXValue`](../) Instanz derString Typ.

```csharp
public static ChartXValue FromString(string value)
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

### Siehe auch

* class [ChartXValue](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
