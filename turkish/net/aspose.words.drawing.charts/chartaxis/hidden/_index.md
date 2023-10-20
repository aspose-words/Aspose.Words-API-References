---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words for .NET
description: ChartAxis Hidden mülk. Bu eksenin gizli olup olmadığını belirten bir bayrağı alır veya ayarlar C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

Bu eksenin gizli olup olmadığını belirten bir bayrağı alır veya ayarlar.

```csharp
public bool Hidden { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Grafik eksenlerinin nasıl gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X ekseni için kategorileri ve Y ekseni için ilgili ondalık değerleri içeren özel bir seri ekleyin.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

 // Grafiğin görünümünü basitleştirmek için grafik eksenlerini gizleyin.
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### Ayrıca bakınız

* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
