---
title: AxisBound.IsAuto
second_title: Aspose.Words for .NET API Referansı
description: AxisBound mülk. Eksen sınırının otomatik olarak belirlenmesi gerektiğini belirten bir bayrak döndürür.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/axisbound/isauto/
---
## AxisBound.IsAuto property

Eksen sınırının otomatik olarak belirlenmesi gerektiğini belirten bir bayrak döndürür.

```csharp
public bool IsAuto { get; }
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


