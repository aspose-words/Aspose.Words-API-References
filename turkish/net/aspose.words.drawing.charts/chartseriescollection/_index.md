---
title: Class ChartSeriesCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.ChartSeriesCollection sınıf. Bir koleksiyonu temsil ederChartSeries .
type: docs
weight: 790
url: /tr/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Bir koleksiyonu temsil eder[`ChartSeries`](../chartseries/) .

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | Sayıyı döndürür[`ChartSeries`](../chartseries/) bu koleksiyonda. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Bir değeri döndürür[`ChartSeries`](../chartseries/) belirtilen dizinde. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(string, DateTime[], double[]) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Her türlü Alan, Radar ve Hisse senedi grafiğine seri eklemek için bu yöntemi kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(string, double[], double[]) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Herhangi bir Dağılım grafiği türüne seri eklemek için bu yöntemi kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(string, string[], double[]) | Yeni ekler[`ChartSeries`](../chartseries/) bu koleksiyona. Herhangi bir Çubuk, Sütun, Çizgi ve Yüzey grafiğine seri eklemek için bu yöntemi kullanın. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(string, double[], double[], double[]) | Yeni ekler[`ChartSeries`](../chartseries/)bu koleksiyona. Herhangi bir Kabarcık grafiği türüne seri eklemek için bu yöntemi kullanın. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Tümünü kaldırır[`ChartSeries`](../chartseries/) bu koleksiyondan. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(int) | Bir'i kaldırır[`ChartSeries`](../chartseries/) belirtilen dizinde. |

### Örnekler

Bir grafiğe seri verilerinin nasıl eklenip kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varsayılan olarak üç dizi demo verisi içerecek bir sütun grafiği ekleyin.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Her serinin dört ondalık değeri vardır: dört kategorinin her biri için bir tane.
// Üç sütundan oluşan dört küme bu verileri temsil edecek.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Grafikteki her serinin adını yazdırın.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Bunlar grafikteki kategorilerin adlarıdır.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Mevcut kategoriler için yeni değerlere sahip bir seri ekleyebiliriz.
// Bu grafik artık dört sütundan oluşan dört küme içerecek.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Bir grafik serisi bu şekilde indekse göre de kaldırılabilir.
// Bu, grafikle birlikte gelen üç demo serisinden birini kaldıracaktır.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Bu yöntemle grafiğin tüm verilerini tek seferde de temizleyebiliriz.
// Yeni bir grafik oluştururken tüm demo verilerini silmenin yolu budur
// boş bir grafik üzerinde çalışmaya başlamadan önce.
chartData.Clear();
```

### Ayrıca bakınız

* class [ChartSeries](../chartseries/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)


