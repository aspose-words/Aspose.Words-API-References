---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: .NET için Aspose.Words
description: ChartLegendEntry IsHidden özelliğini keşfedin, grafik efsanesinin görünürlüğünü zahmetsizce kontrol edin. Bu basit geçiş özelliğiyle veri sunumunuzu geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

Bu girdinin grafik efsanesinde gizli olup olmadığını belirten bir değer alır veya ayarlar. Varsayılan değer**YANLIŞ** .

```csharp
public bool IsHidden { get; set; }
```

## Notlar

Bir grafik efsanesi girişi gizlendiğinde, grafikte hala görüntülenen ilgili grafik serisi veya trend çizgisi etkilenmez.

## Örnekler

Grafik serileri için bir gösterge girişiyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Ayrıca bakınız

* class [ChartLegendEntry](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
