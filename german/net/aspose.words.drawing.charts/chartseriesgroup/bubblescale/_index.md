---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words für .NET
description: Entdecken Sie die BubbleScale-Eigenschaft von ChartSeriesGroup, um die Blasengrößen in Ihren Diagrammen anzupassen und so die Datenvisualisierung und die Benutzerinteraktion zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

Ruft die Größe der Blasen als Prozentsatz ihrer Standardgröße ab oder legt sie fest.

```csharp
public int BubbleScale { get; set; }
```

## Bemerkungen

Gilt nur für Seriengruppen derBubble und Bubble3D Typen.

Der zulässige Wertebereich liegt zwischen 0 und 300 (einschließlich). Der Standardwert ist 100.

## Beispiele

Zeigen Sie, wie Sie die Größe der Blasen einstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein 3D-Blasendiagramm ein.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Blasenskala auf 200 % einstellen.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### Siehe auch

* class [ChartSeriesGroup](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
