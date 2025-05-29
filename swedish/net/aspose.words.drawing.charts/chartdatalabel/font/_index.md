---
title: ChartDataLabel.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: Upptäck teckensnittsegenskapen ChartDataLabel för att enkelt anpassa teckensnittsformateringen för din dataetikett för förbättrad visuell attraktionskraft och tydlighet.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

Ger åtkomst till teckensnittsformateringen för denna dataetikett.

```csharp
public Font Font { get; }
```

## Exempel

Visar hur man använder 3D-effekter med bubbeldiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Använd en dataetikett för varje bubbla som visar dess diameter.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Se även

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
