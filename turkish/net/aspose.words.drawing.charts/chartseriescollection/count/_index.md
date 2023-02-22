---
title: ChartSeriesCollection.Count
second_title: Aspose.Words for .NET API Referansı
description: ChartSeriesCollection mülk. Sayısını döndürürChartSeries bu koleksiyonda.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartseriescollection/count/
---
## ChartSeriesCollection.Count property

Sayısını döndürür[`ChartSeries`](../../chartseries/) bu koleksiyonda.

```csharp
public int Count { get; }
```

### Örnekler

Bir grafikte seri verilerinin nasıl ekleneceğini ve kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varsayılan olarak üç dizi demo verisi içerecek bir sütun grafiği ekleyin.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Her serinin dört ondalık değeri vardır: dört kategorinin her biri için bir tane.
// Üç sütundan oluşan dört küme bu verileri temsil edecektir.
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

// Bunlar grafikteki kategorilerin isimleridir.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Mevcut kategoriler için yeni değerler içeren bir dizi ekleyebiliriz.
// Bu grafik şimdi dört sütundan oluşan dört küme içerecek.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });

// Bir grafik serisi, bunun gibi dizine göre de kaldırılabilir.
// Bu, grafikle birlikte gelen üç demo serisinden birini kaldıracaktır.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));

// Ayrıca bu yöntemle tüm grafiğin verilerini bir kerede temizleyebiliriz.
// Yeni bir grafik oluştururken, tüm demo verilerini silmenin yolu budur
// boş bir grafik üzerinde çalışmaya başlamadan önce.
chartData.Clear();
```

### Ayrıca bakınız

* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* toplantı [Aspose.Words](../../../)


