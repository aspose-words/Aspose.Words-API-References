---
title: ChartLegend.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words für .NET
description: ChartLegend Overlay eigendom. Legt fest ob andere Diagrammelemente die Legende überlappen dürfen. Der Standardwert istFALSCH  in C#.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

Legt fest, ob andere Diagrammelemente die Legende überlappen dürfen. Der Standardwert ist`FALSCH` .

```csharp
public bool Overlay { get; set; }
```

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

// Die Legende des Diagramms in die obere rechte Ecke verschieben.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Geben Sie anderen Diagrammelementen, z. B. dem Diagramm, mehr Platz, indem Sie ihnen erlauben, die Legende zu überlappen.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Siehe auch

* class [ChartLegend](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
