---
title: ChartAxis.MinorUnitIsAuto
linktitle: MinorUnitIsAuto
articleTitle: MinorUnitIsAuto
second_title: Aspose.Words für .NET
description: ChartAxis MinorUnitIsAuto eigendom. Ruft ein Flag ab oder setzt es das angibt ob der Standardabstand zwischen kleinen Teilstrichen verwendet werden soll in C#.
type: docs
weight: 170
url: /de/net/aspose.words.drawing.charts/chartaxis/minorunitisauto/
---
## ChartAxis.MinorUnitIsAuto property

Ruft ein Flag ab oder setzt es, das angibt, ob der Standardabstand zwischen kleinen Teilstrichen verwendet werden soll.

```csharp
public bool MinorUnitIsAuto { get; set; }
```

## Bemerkungen

Die Eigenschaft wirkt sich auf Zeitkategorie und Werteachsen aus.

## Beispiele

Zeigt, wie die Teilstriche und angezeigten Werte einer Diagrammachse manipuliert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Setzen Sie die kleinen Teilstriche der Y-Achse so, dass sie vom Plotbereich weg zeigen.
// und die großen Markierungen, um die Achse zu kreuzen.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Stellen Sie die Y-Achse so ein, dass alle 10 Einheiten ein großer Tick und alle 1 Einheit ein kleiner Tick angezeigt wird.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Setze die Grenzen der Y-Achse auf -10 und 20.
// Auf dieser Y-Achse werden nun 4 große Teilstriche und 27 kleine Teilstriche angezeigt.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Setzen Sie für die X-Achse alle 10 Einheiten die Hauptteilstriche.
// jeder kleine Teilstrich bei 2,5 Einheiten.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Konfigurieren Sie beide Arten von Teilstrichen so, dass sie im Diagrammbereich angezeigt werden.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Legen Sie die Grenzen der X-Achse so fest, dass die X-Achse 5 große Teilstriche und 12 kleine Teilstriche umfasst.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Stellen Sie die Tick-Beschriftungen so ein, dass ihr Wert in Millionen angezeigt wird.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Wir können einen spezifischeren Wert festlegen, anhand dessen Tick-Beschriftungen ihre Werte anzeigen.
// Diese Anweisung entspricht der obigen.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Siehe auch

* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
