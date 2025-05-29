---
title: ChartSeriesGroup.AxisX
linktitle: AxisX
articleTitle: AxisX
second_title: .NET için Aspose.Words
description: ekseni özelliklerine kolay erişim için ChartSeriesGroup AxisX özelliğini keşfedin, veri görselleştirme ve analiz deneyiminizi geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/chartseriesgroup/axisx/
---
## ChartSeriesGroup.AxisX property

Bu seri grubunun X ekseninin özelliklerine erişim sağlar.

```csharp
public ChartAxis AxisX { get; }
```

## Örnekler

Grafikte ikincil eksenle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Varsayılan olarak oluşturulan seriyi sil.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Satır tipinde ek bir seri grubu oluştur.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Yeni seri grubu için ikincil eksenlerin kullanımını belirtin.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// İkincil X eksenini gizle.
newSeriesGroup.AxisX.Hidden = true;
// İkincil Y ekseninin başlığını tanımlayın.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Yeni seri grubuna bir seri ekle.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Ayrıca bakınız

* class [ChartAxis](../../chartaxis/)
* class [ChartSeriesGroup](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
