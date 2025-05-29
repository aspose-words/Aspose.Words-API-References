---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: ChartSeriesCollection Ekleme yöntemiyle grafiklerinizi zahmetsizce geliştirin. Dinamik görseller için Çubuk, Sütun, Çizgi ve Yüzey grafiklerine sorunsuz bir şekilde yeni seriler ekleyin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_5}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Herhangi bir Çubuk, Sütun, Çizgi ve Yüzey grafiğine seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Geri dönüş değeri

Son eklenenler[`ChartSeries`](../../chartseries/) nesne.

## Örnekler

Pareto grafiğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pareto grafiğini ekleyin.
Shape shape = builder.InsertChart(ChartType.Pareto, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Best-Selling Car";

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Bir seri ekle.
chart.Series.Add(
    "Best-Selling Car",
    new string[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
    new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

doc.Save(ArtifactsDir + "Charts.Pareto.docx");
```

Huni grafiğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Huni grafiği ekleyin.
Shape shape = builder.InsertChart(ChartType.Funnel, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Population by Age Group";

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Bir seri ekle.
ChartSeries series = chart.Series.Add(
    "Population by Age Group",
    new string[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
    new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

// Veri etiketlerini göster.
series.HasDataLabels = true;
string decimalSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyDecimalSeparator;
series.DataLabels.NumberFormat.FormatCode = $"0{decimalSeparator}0%";

doc.Save(ArtifactsDir + "Charts.Funnel.docx");
```

Kutu ve bıyık grafiğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Kutu ve Bıyık grafiği ekleyin.
Shape shape = builder.InsertChart(ChartType.BoxAndWhisker, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Points by Years";

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Bir seri ekle.
ChartSeries series = chart.Series.Add(
    "Points by Years",
    new string[]
    {
        "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC",
        "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR",
        "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA"
    },
    new double[]
    {
        91, 80, 100, 77, 90, 104, 105, 118, 120, 101,
        114, 107, 110, 60, 79, 78, 77, 102, 101, 113,
        94, 93, 84, 71, 80, 103, 80, 94, 100, 101
    });

// Veri etiketlerini göster.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.BoxAndWhisker.docx");
```

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add_2}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Herhangi bir Dağılım grafiği türüne seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Geri dönüş değeri

Son eklenenler[`ChartSeries`](../../chartseries/) nesne.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_4}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Herhangi bir Alan, Radar ve Hisse Senedi grafiğine seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_3}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Herhangi bir türdeki Balon grafiklerine seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Geri dönüş değeri

Son eklenenler[`ChartSeries`](../../chartseries/) nesne.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, ChartMultilevelValue[], double[]*) {#add}

Yeni ekler[`ChartSeries`](../../chartseries/)bu koleksiyona. Çok düzeyli veri kategorilerine sahip serileri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, ChartMultilevelValue[] categories, double[] values)
```

### Geri dönüş değeri

Son eklenenler[`ChartSeries`](../../chartseries/) nesne.

## Örnekler

Güneş patlaması grafiğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Sunburst grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Sunburst, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Sales";

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Bir seri ekle.
ChartSeries series = chart.Series.Add(
    "Sales",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Sales - Europe", "UK", "London Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Liverpool Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Manchester Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Paris Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Lyon Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Denver Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Seattle Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Detroit Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Houston Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Toronto Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Montreal Dep."),
        new ChartMultilevelValue("Sales - Oceania", "Australia", "Sydney Dep."),
        new ChartMultilevelValue("Sales - Oceania", "New Zealand", "Auckland Dep.")
    },
    new double[] { 1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694 });

// Veri etiketlerini göster.
series.HasDataLabels = true;
series.DataLabels.ShowValue = false;
series.DataLabels.ShowCategoryName = true;

doc.Save(ArtifactsDir + "Charts.Sunburst.docx");
```

Ağaç haritası grafiğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Treemap grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Bir seri ekle.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// Veri etiketlerini göster.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Ayrıca bakınız

* class [ChartSeries](../../chartseries/)
* class [ChartMultilevelValue](../../chartmultilevelvalue/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, double[]*) {#add_1}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Bu yöntemi Histogram grafiklerine seri eklemek için kullanın.

```csharp
public ChartSeries Add(string seriesName, double[] xValues)
```

### Geri dönüş değeri

Son eklenenler[`ChartSeries`](../../chartseries/) nesne.

## Notlar

Histogram dışındaki grafik türleri için bu yöntem, boş Y değerlerine sahip bir seri ekler.

## Örnekler

Histogram grafiğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Histogram grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Histogram, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Avg Temperature since 1991";

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Bir seri ekle.
chart.Series.Add(
    "Avg Temperature",
    new double[]
    {
        51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4,
        53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7,
        56.3, 55.9, 55.6
    });

doc.Save(ArtifactsDir + "Charts.Histogram.docx");
```

### Ayrıca bakınız

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, string[], double[], bool[]*) {#add_6}

Yeni ekler[`ChartSeries`](../../chartseries/) bu koleksiyona. Şelale grafiklerine seri eklemek için bu yöntemi kullanın.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values, bool[] isSubtotal)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| seriesName | String | Eklenmesi gereken bir dizi ismi. |
| categories | String[] | X ekseni için kategori adları. |
| values | Double[] | Y ekseni değerleri. |
| isSubtotal | Boolean[] | Karşılık gelen Y değerinin ara toplam olup olmadığını gösteren değerler. |

### Geri dönüş değeri

Son eklenenler[`ChartSeries`](../../chartseries/) nesne.

## Notlar

Şelale dışındaki grafik türleri için,*isSubtotal* değerler göz ardı edilir.

## Örnekler

Şelale grafiğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Şelale grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Bir seri ekle.
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

// Veri etiketlerini göster.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.Waterfall.docx");
```

### Ayrıca bakınız

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
