---
title: ChartAxis.AxisBetweenCategories
second_title: Aspose.Words für .NET-API-Referenz
description: ChartAxis eigendom. Ruft ein Flag ab oder setzt es das angibt ob die Wertachse die Kategorieachse zwischen Kategorien kreuzt.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Ruft ein Flag ab oder setzt es, das angibt, ob die Wertachse die Kategorieachse zwischen Kategorien kreuzt.

```csharp
public bool AxisBetweenCategories { get; set; }
```

### Bemerkungen

Die Eigenschaft hat nur Auswirkungen auf Wertachsen. Es wird von den neuen Diagrammen von MS Office 2016 nicht unterstützt.

### Beispiele

Zeigt, wie eine Diagrammachse an einer benutzerdefinierten Position gekreuzt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Bei Säulendiagrammen kreuzt die Y-Achse standardmäßig den Nullpunkt.
// was bedeutet, dass die Spalten für alle Werte unter Null nach unten zeigen, um negative Werte darzustellen.
// Wir können einen anderen Wert für die Kreuzung der Y-Achse festlegen. In diesem Fall setzen wir den Wert auf 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Siehe auch

* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartaxis/)
* Montage [Aspose.Words](../../../)


