---
title: ChartAxisType Enum
linktitle: ChartAxisType
articleTitle: ChartAxisType
second_title: .NET için Aspose.Words
description: Grafik eksen türlerini kolayca tanımlamak ve belgenizin veri görselleştirmesini geliştirmek için Aspose.Words.Drawing.Charts.ChartAxisType enum'unu keşfedin.
type: docs
weight: 920
url: /tr/net/aspose.words.drawing.charts/chartaxistype/
---
## ChartAxisType enumeration

Grafik ekseninin türünü belirtir.

```csharp
public enum ChartAxisType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Category | `0` | Bir grafiğin kategori ekseni. |
| Series | `1` | Bir grafiğin seri ekseni. |
| Value | `2` | Bir grafiğin değer ekseni. |

## Örnekler

Bir grafik türü için uygun türde bir grafik serisinin nasıl oluşturulacağını gösterir.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir grafiğin seri koleksiyonunu doldurmanın birkaç yolu vardır.
    // Farklı grafik tipleri için farklı seri şemaları tasarlanmıştır.
    // 1 - Sütunların X ekseninde kategoriye göre gruplandırıldığı ve bantlandığı sütun grafiği:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Her bir kategori için bir değer içeren iki ondalık değer serisi ekle.
    // Bu sütun grafiği, her biri iki sütundan oluşan üç gruba sahip olacak.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Kategoriler X ekseni boyunca, değerler ise Y ekseni boyunca dağıtılır.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - X ekseni boyunca dağıtılmış tarihlere sahip alan grafiği:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Her bir tarih için ondalık değer içeren bir seri ekle.
    // Tarihler doğrusal bir X ekseni boyunca dağıtılacak,
    // ve bu seriye eklenen değerler veri noktaları oluşturacaktır.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D dağılım grafiği:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Her serinin eşit uzunlukta iki ondalık dizisine ihtiyacı olacak.
    // İlk dizi X değerlerini, ikinci dizi ise karşılık gelen Y değerlerini içerir
    // grafiğin grafiğindeki veri noktalarının.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Balon grafiği:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Her serinin eşit uzunlukta üç ondalık dizisine ihtiyacı olacak.
    // İlk dizi X değerlerini içerir, ikinci dizi karşılık gelen Y değerlerini içerir,
    // ve üçüncüsü, grafiğin her bir veri noktasının çaplarını içerir.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Belirtilen ChartType, genişlik ve yükseklikte bir grafik eklemek ve demo verilerini kaldırmak için belge oluşturucuyu kullanın.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
