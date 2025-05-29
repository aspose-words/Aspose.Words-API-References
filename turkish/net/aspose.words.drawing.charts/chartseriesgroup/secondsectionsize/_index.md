---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: .NET için Aspose.Words
description: Pasta grafiğinizin ikincil bölüm boyutunu etkili bir şekilde özelleştirmek için ChartSeriesGroup'taki SecondSectionSize özelliğini nasıl ayarlayacağınızı keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

Pasta grafiğinin ikincil bölümünün boyutunu yüzde olarak alır veya ayarlar.

```csharp
public int SecondSectionSize { get; set; }
```

## Notlar

Seri gruplarına uygulanırPieOfPie ve PieOfBar türleri.

Kabul edilebilir değerler aralığı 5 ile 200 arasındadır. Varsayılan değer 75'tir.

## Örnekler

Pasta grafiğinin nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// Pasta grafiğinin pastasını biçimlendir.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### Ayrıca bakınız

* class [ChartSeriesGroup](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
