---
title: ChartSeries.CopyFormatFrom
linktitle: CopyFormatFrom
articleTitle: CopyFormatFrom
second_title: Aspose.Words för .NET
description: Upptäck ChartSeries CopyFormatFrom-metoden för att enkelt replikera datapunktsformat efter index, vilket förbättrar din diagrameffektivitet och konsekvens.
type: docs
weight: 190
url: /sv/net/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries.CopyFormatFrom method

Kopierar standardformatet för datapunkten från datapunkten med det angivna indexet.

```csharp
public void CopyFormatFrom(int dataPointIndex)
```

## Exempel

Visar hur man kopierar datapunktsformat.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// Hämta diagrammet och serierna för att uppdatera formatet.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// Kopiera formatet för datapunkten med index 1 till datapunkten med index 2
// så att datapunkt 2 ser likadan ut som datapunkt 1.
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// Kopiera formatet för datapunkten med index 0 till seriens standardvärden så att alla datapunkter
// i serierna som har standardformatet ser de ut likadana som datapunkt 0.
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### Se även

* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
