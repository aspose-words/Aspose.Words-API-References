---
title: Chart.Axes
second_title: Aspose.Words for .NET API Referansı
description: Chart mülk. Bu grafiğin tüm eksenlerinin bir koleksiyonunu alır.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Bu grafiğin tüm eksenlerinin bir koleksiyonunu alır.

```csharp
public ChartAxisCollection Axes { get; }
```

### Örnekler

Eksen koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// Birincil ve ikincil Y eksenlerindeki ana ızgara çizgilerini gizleyin.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Ayrıca bakınız

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chart/)
* toplantı [Aspose.Words](../../../)


