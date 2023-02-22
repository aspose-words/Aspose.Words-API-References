---
title: Class AxisScaling
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.AxisScaling sınıf. Eksenin ölçekleme seçeneklerini temsil eder.
type: docs
weight: 560
url: /tr/net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

Eksenin ölçekleme seçeneklerini temsil eder.

```csharp
public class AxisScaling
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [AxisScaling](axisscaling/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | Logaritmik eksen için logaritmik tabanı alır veya ayarlar. |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | Eksenin maksimum değerini alır veya ayarlar. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | Eksenin minimum değerini alır veya ayarlar. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | Eksenin ölçekleme türünü alır veya ayarlar. |

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)


