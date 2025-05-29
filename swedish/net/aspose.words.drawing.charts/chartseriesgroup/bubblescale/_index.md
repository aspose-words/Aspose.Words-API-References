---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeriesGroup BubbleScale för att anpassa bubbelstorlekar i dina diagram, vilket förbättrar datavisualisering och användarengagemang.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

Hämtar eller ställer in storleken på bubblorna som en procentandel av deras standardstorlek.

```csharp
public int BubbleScale { get; set; }
```

## Anmärkningar

Gäller endast seriegrupper avBubble och Bubble3D typer.

Intervallet för acceptabla värden är från 0 till 300. Standardvärdet är 100.

## Exempel

Visa hur man ställer in storleken på bubblorna.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett bubbeldiagram i 3D.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Ställ in bubbelskalan till 200 %.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### Se även

* class [ChartSeriesGroup](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
