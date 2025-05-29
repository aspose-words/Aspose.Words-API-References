---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: .NET için Aspose.Words
description: Grafik serilerindeki X değerlerini tanımlamak ve veri görselleştirmeyi zahmetsizce geliştirmek için çözümünüz olan Aspose.Words.Drawing.Charts.ChartXValue sınıfını keşfedin.
type: docs
weight: 1160
url: /tr/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Bir grafik serisi için bir X değerini temsil eder.

```csharp
public class ChartXValue
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Depolanan tarih/saat değerini alır. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Depolanan sayısal değeri alır. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Depolanan çok düzeyli değeri alır. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Depolanan dize değerini alır. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Depolanan zaman değerini alır. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Nesnede depolanan X değerinin türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | Bir tane oluşturur`ChartXValue` örneğiDateTime tür. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | Bir tane oluşturur`ChartXValue` örneğiDouble tür. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | Bir tane oluşturur`ChartXValue` örneğiMultilevel tür. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | Bir tane oluşturur`ChartXValue` örneğiString tür. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | Bir tane oluşturur`ChartXValue` örneğiTime tür. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | Belirtilen nesnenin geçerli X değer nesnesine eşit olup olmadığını gösteren bir bayrak alır. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Mevcut X değer nesnesi için bir karma kodu alır. |

## Notlar

Bu sınıf, belirli bir türün X değerini oluşturmak için bir dizi statik yöntem içerir. The [`ValueType`](./valuetype/) özelliği, mevcut bir X değerinin türünü belirlemenize olanak tanır.

Bir grafik serisinin tüm boş olmayan X değerleri aynı olmalıdır[`ChartXValueType`](../chartxvaluetype/) tip.

## Örnekler

Grafik serilerinin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();

// Seriyi verilerle doldur.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// İkinci serinin X ve Y değerlerini temizle.
series2.Clear();

// Seriyi verilerle doldur.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
