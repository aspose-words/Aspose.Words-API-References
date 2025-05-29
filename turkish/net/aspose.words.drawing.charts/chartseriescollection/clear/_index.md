---
title: ChartSeriesCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: .NET için Aspose.Words
description: ChartSeriesCollection Clear yöntemi ile koleksiyonunuzdaki tüm ChartSeries'leri zahmetsizce temizleyin. Veri yönetiminizi bugün kolaylaştırın!
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartseriescollection/clear/
---
## ChartSeriesCollection.Clear method

Tümünü kaldırır[`ChartSeries`](../../chartseries/) bu koleksiyondan.

```csharp
public void Clear()
```

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

* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
