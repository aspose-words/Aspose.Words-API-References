---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ChartAxis AxisBetweenCategories“ – steuern Sie die Positionierung der Werteachse für eine verbesserte Kategorievisualisierung in Ihren Diagrammen. Optimieren Sie Ihre Datenpräsentation!
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Ruft ein Flag ab oder legt es fest, das angibt, ob die Werteachse die Kategorieachse zwischen Kategorien schneidet.

```csharp
public bool AxisBetweenCategories { get; set; }
```

## Bemerkungen

Die Eigenschaft wirkt sich nur auf Werteachsen aus. Sie wird von den neuen Diagrammen in MS Office 2016 nicht unterstützt.

## Beispiele

Zeigt, wie man eine Diagrammachse an einer benutzerdefinierten Stelle kreuzen kann.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Bei Säulendiagrammen kreuzt sich die Y-Achse standardmäßig bei Null,
// was bedeutet, dass die Spalten für alle Werte unter Null nach unten zeigen, um negative Werte darzustellen.
// Wir können einen anderen Wert für den Schnittpunkt der Y-Achse festlegen. In diesem Fall setzen wir ihn auf 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Siehe auch

* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
