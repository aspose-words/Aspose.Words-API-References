---
title: ChartSeriesCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: ChartSeriesCollection Item mülk. Bir değeri döndürürChartSeries belirtilen dizinde C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/chartseriescollection/item/
---
## ChartSeriesCollection indexer

Bir değeri döndürür[`ChartSeries`](../../chartseries/) belirtilen dizinde.

```csharp
public ChartSeries this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyona bir dizin. |

## Notlar

Endeks sıfır bazlıdır.

Negatif dizinlere izin verilir ve koleksiyonun arkasından erişimi belirtir. Örneğin -1 son öğe anlamına gelir, -2 sondan önceki ikinci öğe anlamına gelir ve bu şekilde devam eder.

Dizin listedeki öğe sayısından büyük veya ona eşitse bu, boş bir başvuru döndürür.

Dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse bu, boş bir başvuru döndürür.

## Örnekler

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
