---
title: ChartAxis.Type
second_title: Aspose.Words for .NET API Referansı
description: ChartAxis mülk. Eksenin türünü döndürür.
type: docs
weight: 290
url: /tr/net/aspose.words.drawing.charts/chartaxis/type/
---
## ChartAxis.Type property

Eksenin türünü döndürür.

```csharp
public ChartAxisType Type { get; }
```

### Örnekler

Bir grafik türü için uygun türde bir grafik serisinin nasıl oluşturulacağını gösterir.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir grafiğin seri koleksiyonunu doldurmanın birkaç yolu vardır.
    // Farklı seri şemaları, farklı grafik türleri için tasarlanmıştır.
    // 1 - X ekseni boyunca kategoriye göre gruplandırılmış ve şeritlenmiş sütunlara sahip sütun grafiği:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // İlgili her kategori için bir değer içeren iki ondalık değer serisi ekleyin.
    // Bu sütun grafiğinde her biri iki sütunlu üç grup bulunacaktır.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Kategoriler X ekseni boyunca, değerler ise Y ekseni boyunca dağıtılır.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Tarihlerin X ekseni boyunca dağıtıldığı alan grafiği:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // İlgili her tarih için ondalık değere sahip bir seri ekleyin.
    // Tarihler doğrusal bir X ekseni boyunca dağıtılacak,
    // ve bu seriye eklenen değerler veri noktaları oluşturacaktır.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2B dağılım grafiği:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Her serinin eşit uzunlukta iki ondalık diziye ihtiyacı olacaktır.
    // İlk dizi X değerlerini içerir ve ikincisi karşılık gelen Y değerlerini içerir
    // grafiğin grafiğindeki veri noktalarının.
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

    // Her serinin eşit uzunlukta üç ondalık diziye ihtiyacı olacaktır.
    // İlk dizi X değerlerini içerir, ikincisi karşılık gelen Y değerlerini içerir,
    // ve üçüncüsü grafiğin veri noktalarının her biri için çapları içerir.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Belirtilen ChartType, genişlik ve yükseklikteki belge oluşturucuyu kullanarak bir grafik ekleyin ve demo verilerini kaldırın.
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

* enum [ChartAxisType](../../chartaxistype/)
* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartaxis/)
* toplantı [Aspose.Words](../../../)


