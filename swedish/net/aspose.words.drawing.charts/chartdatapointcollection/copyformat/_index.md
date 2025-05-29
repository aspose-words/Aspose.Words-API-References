---
title: ChartDataPointCollection.CopyFormat
linktitle: CopyFormat
articleTitle: CopyFormat
second_title: Aspose.Words för .NET
description: Kopiera enkelt formatering mellan datapunkter med metoden ChartDataPointCollection CopyFormat. Förbättra din datavisualisering idag!
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/chartdatapointcollection/copyformat/
---
## ChartDataPointCollection.CopyFormat method

Kopierar format från källdatapunkten till destinationsdatapunkten.

```csharp
public void CopyFormat(int sourceIndex, int destinationIndex)
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

* class [ChartDataPointCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
