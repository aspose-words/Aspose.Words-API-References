---
title: ChartDataLabel.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft ShowBubbleSize Ihre Blasendiagramme durch die Anzeige von Datenbeschriftungsgrößen verbessert. Optimieren Sie noch heute Ihre visuelle Datendarstellung!
type: docs
weight: 130
url: /de/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

Ermöglicht die Angabe, ob die Blasengröße für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Gilt nur für Blasendiagramme. Der Standardwert ist`FALSCH` .

```csharp
public bool ShowBubbleSize { get; set; }
```

## Beispiele

Zeigt, wie 3D-Effekte mit Blasendiagrammen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Wenden Sie auf jede Blase eine Datenbeschriftung an, die ihren Durchmesser anzeigt.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Siehe auch

* class [ChartDataLabel](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
