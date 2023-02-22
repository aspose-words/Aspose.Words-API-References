---
title: AxisBound.AxisBound
second_title: Aspose.Words for .NET API Referansı
description: AxisBound inşaatçı. Eksen sınırının bir sözcük işleme uygulaması tarafından otomatik olarak belirlenmesi gerektiğini belirten yeni bir örnek oluşturur.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound() {#constructor}

Eksen sınırının bir sözcük işleme uygulaması tarafından otomatik olarak belirlenmesi gerektiğini belirten yeni bir örnek oluşturur.

```csharp
public AxisBound()
```

### Örnekler

Özel eksen sınırlarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// İki ondalık dizi içeren bir dizi ekleyin. İlk dizi, X değerlerini içerir,
// ve ikincisi, dağılım grafiğindeki noktalar için karşılık gelen Y değerlerini içerir.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// Varsayılan olarak, grafiğin X ve Y eksenlerine varsayılan ölçekleme uygulanır,
// böylece her iki aralığı da her serinin her X ve Y değerini kapsayacak kadar büyük.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Kendi eksen sınırlarımızı tanımlayabiliriz.
// Bu durumda hem X hem de Y ekseni cetvellerinin 0 ile 10 arasında bir aralık göstermesini sağlayacağız.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// X ekseninde bir tarih aralığı ve Y ekseni için ondalık değerler gerektiren bir dizi içeren bir çizgi grafik oluşturun.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// Eksen sınırlarını tarih şeklinde de ayarlayarak grafiği bir nokta ile sınırlayabiliriz.
// Aralığı 1980-1990 olarak ayarlamak, seri değerlerinden ikisini atlayacaktır.
// grafikteki aralığın dışında olanlar.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Ayrıca bakınız

* class [AxisBound](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../axisbound/)
* toplantı [Aspose.Words](../../../)

---

## AxisBound(double) {#constructor_1}

Sayı olarak gösterilen bir eksen sınırı oluşturur.

```csharp
public AxisBound(double value)
```

### Örnekler

Tarih/saat değerleriyle grafiğin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X ekseni için tarih/saat değerlerini ve Y ekseni için ilgili ondalık değerleri içeren özel bir seri ekleyin.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// X ekseni için alt ve üst sınırları ayarlayın.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// X ekseninin ana birimlerini bir haftaya ve küçük birimleri bir güne ayarlayın.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// Ondalık değerler için Y ekseni özelliklerini tanımlayın.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Ayrıca bakınız

* class [AxisBound](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../axisbound/)
* toplantı [Aspose.Words](../../../)

---

## AxisBound(DateTime) {#constructor_2}

Tarih saat değeri olarak temsil edilen bir eksen sınırı oluşturur.

```csharp
public AxisBound(DateTime datetime)
```

### Örnekler

Tarih/saat değerleriyle grafiğin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X ekseni için tarih/saat değerlerini ve Y ekseni için ilgili ondalık değerleri içeren özel bir seri ekleyin.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// X ekseni için alt ve üst sınırları ayarlayın.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// X ekseninin ana birimlerini bir haftaya ve küçük birimleri bir güne ayarlayın.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// Ondalık değerler için Y ekseni özelliklerini tanımlayın.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Ayrıca bakınız

* class [AxisBound](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../axisbound/)
* toplantı [Aspose.Words](../../../)


