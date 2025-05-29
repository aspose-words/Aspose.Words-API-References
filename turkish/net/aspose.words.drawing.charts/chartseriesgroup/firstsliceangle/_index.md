---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için pasta grafiğinizin ilk dilim açısını derece cinsinden özelleştirmek üzere ChartSeriesGroup FirstSliceAngle özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

Ana pasta grafiğinin ilk diliminin açısını derece olarak alır veya ayarlar.

```csharp
public int FirstSliceAngle { get; set; }
```

## Notlar

Seri gruplarına uygulanırPie ,Pie3D veDoughnut türleri.

Kabul edilebilir değerler aralığı 0 ile 360 dahil olmak üzeredir. Varsayılan değer 0'dır.

## Örnekler

Halka grafiğinin nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// Çörek grafiğini biçimlendir.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### Ayrıca bakınız

* class [ChartSeriesGroup](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
