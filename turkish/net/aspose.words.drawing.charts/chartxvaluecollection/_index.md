---
title: ChartXValueCollection Class
linktitle: ChartXValueCollection
articleTitle: ChartXValueCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartXValueCollection sınıf. Bir grafik serisi için X değerlerinden oluşan bir koleksiyonu temsil eder C#'da.
type: docs
weight: 850
url: /tr/net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Bir grafik serisi için X değerlerinden oluşan bir koleksiyonu temsil eder.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Bu koleksiyondaki öğelerin sayısını alır. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Belirtilen dizindeki X değerini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |

## Notlar

Koleksiyonun dışındaki tüm öğeleri**hükümsüz** aynısı olmalı[`ValueType`](../chartxvalue/valuetype/).

Koleksiyon yalnızca X değerlerinin değiştirilmesine izin verir. Bir grafik serisine yeni değerler eklemek veya değerleri kaldırmak için uygun yöntemleri kullanın.[`ChartSeries`](../chartseries/) sınıf kullanılabilir.

## Örnekler

Grafik serisi verilerinin nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // Tüm veri noktalarının bireysel formatını temizle.
    // Sütun grafiklerinde veri noktaları ve veri değerleri bire birdir.
    series.DataPoints[i].ClearFormat();

    // Y değerini al.
    double yValue = series.YValues[i].DoubleValue;

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Maksimum ve minimum değerlerin renklerini değiştirin.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### Ayrıca bakınız

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartXValue](../chartxvalue/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
