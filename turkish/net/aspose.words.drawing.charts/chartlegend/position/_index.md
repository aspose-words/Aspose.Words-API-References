---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: .NET için Aspose.Words
description: Grafiklerinizin açıklama yerleşimini daha net ve görsel olarak çekici hale getirmek için ChartLegend Position özelliğini keşfedin ve kolayca özelleştirin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Bir grafikteki efsanenin konumunu belirtir.

```csharp
public LegendPosition Position { get; set; }
```

## Notlar

Varsayılan değer:Right Word 2016 öncesi grafikler ve içinTop Word 2016 grafikleri için.

## Örnekler

Bir grafiğin açıklamasının görünümünün nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Grafiğin açıklamasını sağ üst köşeye taşı.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Grafik gibi diğer grafik öğelerine, açıklamanın üzerine binmelerine izin vererek daha fazla yer verin.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Ayrıca bakınız

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
