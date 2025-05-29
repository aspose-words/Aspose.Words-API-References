---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ChartLegend Position“, um die Platzierung der Legende Ihres Diagramms einfach anzupassen und so die Übersichtlichkeit und Optik zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Gibt die Position der Legende in einem Diagramm an.

```csharp
public LegendPosition Position { get; set; }
```

## Bemerkungen

Der Standardwert istRight für Diagramme vor Word 2016 und Top für Word 2016-Diagramme.

## Beispiele

Zeigt, wie das Erscheinungsbild der Legende eines Diagramms bearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Verschieben Sie die Legende des Diagramms in die obere rechte Ecke.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Geben Sie anderen Diagrammelementen, beispielsweise dem Graphen, mehr Platz, indem Sie zulassen, dass sie die Legende überlappen.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Siehe auch

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
