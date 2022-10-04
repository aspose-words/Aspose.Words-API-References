---
title: Add
second_title: Aspose.Words for .NET API Referansı
description: Yeni eklerChartSeriesaspose.words.drawing.charts/chartseries/bu koleksiyona. Herhangi bir Çubuk Sütun Çizgi ve Yüzey grafiğine seri eklemek için bu yöntemi kullanın.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(string, string[], double[]) {#add_3}

Yeni ekler[`ChartSeries`](../../chartseries/)bu koleksiyona. Herhangi bir Çubuk, Sütun, Çizgi ve Yüzey grafiğine seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Geri dönüş değeri

Son eklenen[`ChartSeries`](../../chartseries/) nesne.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* toplantı [Aspose.Words](../../../)

---

## Add(string, double[], double[]) {#add}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Her tür Dağılım grafiğine seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Geri dönüş değeri

Son eklenen[`ChartSeries`](../../chartseries/) nesne.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* toplantı [Aspose.Words](../../../)

---

## Add(string, DateTime[], double[]) {#add_2}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Her tür Alan, Radar ve Hisse senedi grafiğine seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* toplantı [Aspose.Words](../../../)

---

## Add(string, double[], double[], double[]) {#add_1}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Herhangi bir Bubble grafiği türüne seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Geri dönüş değeri

Son eklenen[`ChartSeries`](../../chartseries/) nesne.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
