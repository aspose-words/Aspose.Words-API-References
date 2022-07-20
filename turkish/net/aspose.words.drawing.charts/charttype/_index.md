---
title: ChartType
second_title: Aspose.Words for .NET API Referansı
description: Bir grafiğin türünü belirtir.
type: docs
weight: 760
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
| Area3D | `3` | 3B Alan grafiği. |
| Area3DStacked | `4` | 3B Yığılmış Alan grafiği. |
| Area3DPercentStacked | `5` | 3D %100 Yığılmış Alan grafiği. |
| Bar | `6` | Çubuk grafik. |
| BarStacked | `7` | Yığılmış Çubuk grafik. |
| BarPercentStacked | `8` | %100 Yığılmış Çubuk grafik. |
| Bar3D | `9` | 3D Çubuk grafik. |
| Bar3DStacked | `10` | 3D Yığılmış Çubuk grafik. |
| Bar3DPercentStacked | `11` | 3D %100 Yığılmış Çubuk grafik. |
| Bubble | `12` | Kabarcık grafiği. |
| Bubble3D | `13` | 3D Kabarcık grafiği. |
| Column | `14` | Sütun grafiği. |
| ColumnStacked | `15` | Yığılmış Sütun grafiği. |
| ColumnPercentStacked | `16` | %100 Yığılmış Sütun grafiği. |
| Column3D | `17` | 3B Sütun grafiği. |
| Column3DStacked | `18` | 3B Yığılmış Sütun grafiği. |
| Column3DPercentStacked | `19` | 3D %100 Yığılmış Sütun grafiği. |
| Column3DClustered | `20` | 3B Kümelenmiş Sütun grafiği. |
| Doughnut | `21` | Halka grafiği. |
| Line | `22` | Çizgi grafik. |
| LineStacked | `23` | Yığılmış Çizgi grafiği. |
| LinePercentStacked | `24` | %100 Yığılmış Çizgi grafiği. |
| Line3D | `25` | 3B Çizgi grafiği. |
| Pie | `26` | Pasta grafik. |
| Pie3D | `27` | 3D Pasta grafiği. |
| PieOfBar | `28` | Çubuk grafiğin pastası. |
| PieOfPie | `29` | Pasta grafiği. |
| Radar | `30` | Radar grafiği. |
| Scatter | `31` | Dağılım grafiği. |
| Stock | `32` | Hisse senedi grafiği. |
| Surface | `33` | Yüzey grafiği. |
| Surface3D | `34` | 3B Yüzey grafiği. |

### Örnekler

Bir grafik türü için uygun bir grafik serisi türünün nasıl oluşturulacağını gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir grafiğin seri koleksiyonunu doldurmanın birkaç yolu vardır.
    // Farklı grafik türleri için farklı seri şemaları amaçlanmıştır.
    // 1 - X ekseni boyunca kategoriye göre gruplandırılmış ve bantlanmış sütunlara sahip sütun grafiği:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Her ilgili kategori için bir değer içeren iki dizi ondalık değer girin.
    // Bu sütun grafiği, her biri iki sütunlu üç gruba sahip olacaktır.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Kategoriler X ekseni boyunca dağıtılır ve değerler Y ekseni boyunca dağıtılır.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Tarihleri X ekseni boyunca dağıtılmış alan grafiği:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Her ilgili tarih için ondalık değere sahip bir dizi ekleyin.
    // Tarihler doğrusal bir X ekseni boyunca dağıtılacak,
    // ve bu seriye eklenen değerler veri noktaları oluşturacaktır.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2B dağılım grafiği:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Her dizi, eşit uzunlukta iki ondalık diziye ihtiyaç duyacaktır.
    // İlk dizi X değerlerini içerir ve ikincisi karşılık gelen Y değerlerini içerir
    // grafiğin grafiğindeki veri noktalarının sayısı.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Kabarcık grafiği:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Her dizi, eşit uzunlukta üç ondalık diziye ihtiyaç duyacaktır.
    // İlk dizi X değerlerini içerir, ikincisi karşılık gelen Y değerlerini içerir,
    // ve üçüncüsü, grafiğin veri noktalarının her biri için çapları içerir.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Belirtilen ChartType, genişlik ve yüksekliğe sahip bir belge oluşturucu kullanarak bir grafik ekleyin ve demo verilerini kaldırın.
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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->