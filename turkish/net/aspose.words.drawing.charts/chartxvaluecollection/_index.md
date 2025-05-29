---
title: ChartXValueCollection Class
linktitle: ChartXValueCollection
articleTitle: ChartXValueCollection
second_title: .NET için Aspose.Words
description: Grafik serilerindeki X değer koleksiyonlarını etkili bir şekilde yönetmek için çözümünüz olan Aspose.Words.Drawing.Charts.ChartXValueCollection sınıfını keşfedin.
type: docs
weight: 1170
url: /tr/net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Bir grafik serisi için X değerlerinin bir koleksiyonunu temsil eder.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Bu koleksiyondaki öğelerin sayısını alır. |
| [FormatCode](../../aspose.words.drawing.charts/chartxvaluecollection/formatcode/) { get; set; } | X değerlerine uygulanan biçim kodunu alır veya ayarlar. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Belirtilen dizindeki X değerini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |

## Notlar

Koleksiyondaki tüm öğeler hariç**hükümsüz** aynı olmalı[`ValueType`](../chartxvalue/valuetype/).

Koleksiyon yalnızca X değerlerini değiştirmeye izin verir. Bir grafik serisine yeni değerler eklemek veya eklemek ya da değerleri kaldırmak için, uygun yöntemler[`ChartSeries`](../chartseries/) sınıf kullanılabilir.

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
    // Sütun grafiklerde veri noktaları ve veri değerleri birebirdir.
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

// Maksimum ve minimum değerlerin renklerini değiştir.
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
