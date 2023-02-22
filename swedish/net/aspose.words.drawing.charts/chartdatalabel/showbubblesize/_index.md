---
title: ChartDataLabel.ShowBubbleSize
second_title: Aspose.Words för .NET API Referens
description: ChartDataLabel fast egendom. Gör det möjligt att ange om bubbelstorlek ska visas för dataetiketterna i ett diagram. Gäller endast för bubbeldiagram. Standardvärdet är falskt.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

Gör det möjligt att ange om bubbelstorlek ska visas för dataetiketterna i ett diagram. Gäller endast för bubbeldiagram. Standardvärdet är falskt.

```csharp
public bool ShowBubbleSize { get; set; }
```

### Exempel

Visar hur man använder 3D-effekter med bubbeldiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Applicera en dataetikett på varje bubbla som visar dess diameter.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Se även

* class [ChartDataLabel](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartdatalabel/)
* hopsättning [Aspose.Words](../../../)


