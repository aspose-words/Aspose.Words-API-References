---
title: ChartSeriesGroup.Series
linktitle: Series
articleTitle: Series
second_title: .NET için Aspose.Words
description: İlgili serilerin benzersiz koleksiyonuna erişmek ve veri görselleştirme deneyiminizi geliştirmek için ChartSeriesGroup Series özelliğini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.drawing.charts/chartseriesgroup/series/
---
## ChartSeriesGroup.Series property

Bu seri grubuna ait serilerin bir koleksiyonunu alır.

```csharp
public ChartSeriesCollection Series { get; }
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

* class [ChartSeriesCollection](../../chartseriescollection/)
* class [ChartSeriesGroup](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
