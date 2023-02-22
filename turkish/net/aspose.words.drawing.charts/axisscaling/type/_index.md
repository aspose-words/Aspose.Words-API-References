---
title: AxisScaling.Type
second_title: Aspose.Words for .NET API Referansı
description: AxisScaling mülk. Eksenin ölçekleme türünü alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/axisscaling/type/
---
## AxisScaling.Type property

Eksenin ölçekleme türünü alır veya ayarlar.

```csharp
public AxisScaleType Type { get; set; }
```

### Notlar

Linear değer, MS Office 2016 yeni çizelgelerinde izin verilen tek değerdir.

### Örnekler

Bir grafik eksenine logaritmik ölçeklendirmenin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// Beş nokta için X/Y koordinatlarına sahip bir dizi ekleyin.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// X ekseninin ölçeklemesi varsayılan olarak doğrusaldır,
// X-değeri aralığımızı (0, 1, 2, 3...) kapsayan eşit artan değerleri görüntülüyor.
// Doğrusal bir eksen, Y değerlerimiz için ideal değil
// çünkü daha küçük Y değerlerine sahip noktaların okunması daha zor olacaktır.
// Tabanı 20 (1, 20, 400, 8000...) olan bir logaritmik ölçekleme
// çizilen noktaları yayarak grafik üzerindeki değerlerini daha kolay okumamızı sağlar.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Ayrıca bakınız

* enum [AxisScaleType](../../axisscaletype/)
* class [AxisScaling](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../axisscaling/)
* toplantı [Aspose.Words](../../../)


