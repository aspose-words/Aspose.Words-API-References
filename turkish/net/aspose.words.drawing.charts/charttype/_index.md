---
title: ChartType Enum
linktitle: ChartType
articleTitle: ChartType
second_title: .NET için Aspose.Words
description: Çeşitli grafik türlerini keşfetmek ve belgenizin veri görselleştirmesini zahmetsizce geliştirmek için Aspose.Words.Drawing.Charts.ChartType enum'unu keşfedin.
type: docs
weight: 1150
url: /tr/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Bir grafiğin türünü belirtir.

```csharp
public enum ChartType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Area | `0` | Alan grafiği. |
| AreaStacked | `1` | Yığılmış Alan grafiği. |
| AreaPercentStacked | `2` | %100 Yığılmış Alan grafiği. |
| Area3D | `3` | 3D Alan grafiği. |
| Area3DStacked | `4` | 3D Yığılmış Alan grafiği. |
| Area3DPercentStacked | `5` | 3D %100 Yığılmış Alan grafiği. |
| Bar | `6` | Çubuk grafik. |
| BarStacked | `7` | Yığılmış Çubuk grafiği. |
| BarPercentStacked | `8` | %100 Yığılmış Çubuk grafiği. |
| Bar3D | `9` | 3D Çubuk Grafik. |
| Bar3DStacked | `10` | 3D Yığılmış Çubuk Grafik. |
| Bar3DPercentStacked | `11` | 3D %100 Yığılmış Çubuk Grafik. |
| Bubble | `12` | Kabarcık grafiği. |
| Bubble3D | `13` | 3D Baloncuk grafiği. |
| Column | `14` | Sütun grafiği. |
| ColumnStacked | `15` | Yığılmış Sütun grafiği. |
| ColumnPercentStacked | `16` | %100 Yığılmış Sütun grafiği. |
| Column3D | `17` | 3D Sütun grafiği. |
| Column3DStacked | `18` | 3D Yığılmış Sütun grafiği. |
| Column3DPercentStacked | `19` | 3D %100 Yığılmış Sütun grafiği. |
| Column3DClustered | `20` | 3D Kümelenmiş Sütun grafiği. |
| Doughnut | `21` | Çörek şeması. |
| Line | `22` | Çizgi grafiği. |
| LineStacked | `23` | Yığılmış Çizgi grafiği. |
| LinePercentStacked | `24` | %100 Yığılmış Çizgi grafiği. |
| Line3D | `25` | 3D Çizgi grafiği. |
| Pie | `26` | Pasta grafiği. |
| Pie3D | `27` | 3D Pasta grafiği. |
| PieOfBar | `28` | Çubuk pasta grafiği. |
| PieOfPie | `29` | Pasta grafiğinin pastası. |
| Radar | `30` | Radar çizelgesi. |
| Scatter | `31` | Dağılım grafiği. |
| Stock | `32` | Hisse senedi grafiği. |
| Surface | `33` | Yüzey grafiği. |
| Surface3D | `34` | 3D Yüzey grafiği. |
| Treemap | `35` | Ağaç haritası grafiği. |
| Sunburst | `36` | Güneş patlaması grafiği. |
| Histogram | `37` | Histogram grafiği. |
| Pareto | `38` | Pareto grafiği. |
| BoxAndWhisker | `39` | Kutu ve Bıyık grafiği. |
| Waterfall | `40` | Şelale grafiği. |
| Funnel | `41` | Huni grafiği. |

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
