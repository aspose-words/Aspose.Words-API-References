---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ChartAxis CrossesAt“, um Schnittpunkte auf der senkrechten Achse Ihres Diagramms einfach zu definieren und so die Datenvisualisierung zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Gibt an, wo auf der senkrechten Achse die Achse kreuzt.

```csharp
public double CrossesAt { get; set; }
```

## Bemerkungen

Die Eigenschaft ist nur dann wirksam, wenn[`Crosses`](../crosses/) sind eingestellt aufCustom. Es wird von den neuen Diagrammen von MS Office 2016 nicht unterstützt.

Die Einheiten werden durch den Achsentyp bestimmt. Bei einer Werteachse ist der Wert der Eigenschaft eine Dezimalzahl auf der Werteachse. Bei einer Zeitkategorieachse ist der Wert definiert als eine ganzzahlige Anzahl von Tagen relativ zum Basisdatum (30.12.1899). Bei einer Textkategorieachse ist der Wert eine ganzzahlige Kategorienummer, beginnend mit 1 als erster Kategorie.

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
