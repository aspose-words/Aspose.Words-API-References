---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: .NET için Aspose.Words
description: Grafik serilerini zahmetsizce yönetmek ve özelleştirmek için çözümünüz olan Aspose.Words.Drawing.Charts.ChartSeriesCollection sınıfını keşfedin.
type: docs
weight: 1080
url: /tr/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Bir koleksiyonu temsil eder[`ChartSeries`](../chartseries/) .

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | sayısını döndürür[`ChartSeries`](../chartseries/) bu koleksiyonda. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Bir[`ChartSeries`](../chartseries/) belirtilen dizinde. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[]*) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Bu yöntemi Histogram grafiklerine seri eklemek için kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, ChartMultilevelValue[], double[]*) | Yeni ekler[`ChartSeries`](../chartseries/)bu koleksiyona. Çok düzeyli veri kategorilerine sahip serileri eklemek için bu yöntemi kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_4)(*string, DateTime[], double[]*) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Herhangi bir Alan, Radar ve Hisse Senedi grafiğine seri eklemek için bu yöntemi kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, double[], double[]*) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Herhangi bir Dağılım grafiği türüne seri eklemek için bu yöntemi kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_5)(*string, string[], double[]*) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Herhangi bir Çubuk, Sütun, Çizgi ve Yüzey grafiğine seri eklemek için bu yöntemi kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, double[], double[], double[]*) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Herhangi bir türdeki Balon grafiklerine seri eklemek için bu yöntemi kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_6)(*string, string[], double[], bool[]*) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Şelale grafiklerine seri eklemek için bu yöntemi kullanın. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Tümünü kaldırır[`ChartSeries`](../chartseries/) bu koleksiyondan. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | Birini kaldırır[`ChartSeries`](../chartseries/) belirtilen dizinde. |

## Örnekler

Bir grafikte seri verilerinin nasıl ekleneceğini ve kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varsayılan olarak üç seri demo verisi içerecek bir sütun grafiği ekleyin.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Her serinin dört ondalık değeri vardır: dört kategorinin her biri için bir değer.
// Bu veriler üç sütundan oluşan dört küme tarafından temsil edilecektir.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Grafikteki her serinin adını yazdır.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Bunlar grafikteki kategorilerin adlarıdır.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Mevcut kategoriler için yeni değerler içeren bir seri ekleyebiliriz.
// Bu grafik artık dört sütundan oluşan dört küme içerecek.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Bir grafik serisi, bu şekilde indekse göre de kaldırılabilir.
// Bu, grafikle birlikte gelen üç demo serisinden birini kaldıracaktır.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Bu yöntemle aynı zamanda grafiğin tüm verilerini tek seferde temizleyebiliriz.
// Yeni bir grafik oluştururken, tüm demo verilerini silmenin yolu budur
// boş bir grafik üzerinde çalışmaya başlamadan önce.
chartData.Clear();
```

### Ayrıca bakınız

* class [ChartSeries](../chartseries/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
