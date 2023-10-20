---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words für .NET
description: ChartAxis CrossesAt eigendom. Gibt an wo sich die Achse auf der senkrechten Achse kreuzt in C#.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Gibt an, wo sich die Achse auf der senkrechten Achse kreuzt.

```csharp
public double CrossesAt { get; set; }
```

## Bemerkungen

Die Eigenschaft ist nur wirksam, wenn[`Crosses`](../crosses/) eingestellt sindCustom. Die neuen Diagramme von MS Office 2016 werden nicht unterstützt.

Die Einheiten werden durch den Achsentyp bestimmt. Wenn es sich bei der Achse um eine Werteachse handelt, ist der Wert der Eigenschaft eine Dezimalzahl auf der Werteachse. Wenn es sich bei der Achse um eine Zeitkategorieachse handelt, wird der Wert als definiert, eine ganzzahlige Anzahl von Tagen relativ zum Basisdatum (30.12.1899). Für eine Textkategorieachse ist der Wert eine ganzzahlige Kategorienummer, beginnend mit 1 als erster Kategorie.

## Beispiele

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
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
