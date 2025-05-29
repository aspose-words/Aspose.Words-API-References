---
title: ChartAxis.MinorUnitIsAuto
linktitle: MinorUnitIsAuto
articleTitle: MinorUnitIsAuto
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft ChartAxis MinorUnitIsAuto die Teilstriche Ihres Diagramms für eine klarere Datenvisualisierung optimiert. Verbessern Sie Ihre Grafiken mühelos!
type: docs
weight: 180
url: /de/net/aspose.words.drawing.charts/chartaxis/minorunitisauto/
---
## ChartAxis.MinorUnitIsAuto property

Ruft ein Flag ab oder legt es fest, das angibt, ob der Standardabstand zwischen kleinen Teilstrichen verwendet werden soll.

```csharp
public bool MinorUnitIsAuto { get; set; }
```

## Bemerkungen

Die Eigenschaft wirkt sich auf Zeitkategorie- und Werteachsen aus.

## Beispiele

Zeigt, wie die Teilstriche und angezeigten Werte einer Diagrammachse bearbeitet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Die kleinen Markierungen der Y-Achse so einstellen, dass sie vom Plotbereich weg zeigen,
// und die Hauptmarkierungen zum Kreuzen der Achse.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Stellen Sie die Y-Achse so ein, dass alle 10 Einheiten ein großer Teilstrich und alle 1 Einheit ein kleiner Teilstrich angezeigt wird.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Setzen Sie die Grenzen der Y-Achse auf -10 und 20.
// Diese Y-Achse zeigt jetzt 4 große und 27 kleine Teilstriche an.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Für die X-Achse die Hauptmarkierungen alle 10 Einheiten setzen,
// jede kleine Markierung bei 2,5 Einheiten.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Konfigurieren Sie beide Arten von Teilstrichen so, dass sie innerhalb des Diagrammbereichs angezeigt werden.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Legen Sie die Grenzen der X-Achse so fest, dass die X-Achse 5 große und 12 kleine Teilstriche umfasst.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// Legen Sie die Teilstrichbeschriftungen so fest, dass ihr Wert in Millionen angezeigt wird.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Wir können einen spezifischeren Wert festlegen, anhand dessen die Werte der Teilstrichbeschriftungen angezeigt werden.
// Diese Anweisung ist gleichwertig mit der obigen.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Siehe auch

* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
