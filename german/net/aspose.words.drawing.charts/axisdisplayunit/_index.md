---
title: AxisDisplayUnit Class
linktitle: AxisDisplayUnit
articleTitle: AxisDisplayUnit
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.AxisDisplayUnit, um die Skalierungsoptionen der Werteachse anzupassen und so die Übersichtlichkeit und Präzision des Diagramms zu verbessern.
type: docs
weight: 790
url: /de/net/aspose.words.drawing.charts/axisdisplayunit/
---
## AxisDisplayUnit class

Bietet Zugriff auf die Skalierungsoptionen der Anzeigeeinheiten für die Werteachse.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class AxisDisplayUnit
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [AxisDisplayUnit](axisdisplayunit/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomUnit](../../aspose.words.drawing.charts/axisdisplayunit/customunit/) { get; set; } | Ruft einen benutzerdefinierten Divisor ab oder legt ihn fest, um die Anzeigeeinheiten auf der Werteachse zu skalieren. |
| [Document](../../aspose.words.drawing.charts/axisdisplayunit/document/) { get; } | Gibt das Dokument zurück, das das übergeordnete Diagramm enthält. |
| [Unit](../../aspose.words.drawing.charts/axisdisplayunit/unit/) { get; set; } | Ruft den Skalierungswert der Anzeigeeinheiten als einen der vordefinierten Werte ab oder legt ihn fest. |

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

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
