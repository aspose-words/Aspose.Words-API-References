---
title: ChartLegend.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words für .NET
description: Steuern Sie die Überlappung von Diagrammelementen mit der ChartLegend-Overlay-Eigenschaft. Verbessern Sie Ihre Datenvisualisierung mit anpassbaren Legendeneinstellungen für klarere Einblicke.
type: docs
weight: 40
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

// Verschieben Sie die Legende des Diagramms in die obere rechte Ecke.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Geben Sie anderen Diagrammelementen, beispielsweise dem Graphen, mehr Platz, indem Sie zulassen, dass sie die Legende überlappen.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Siehe auch

* class [ChartLegend](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
