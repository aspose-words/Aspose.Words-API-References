---
title: AxisScaling.LogBase
linktitle: LogBase
articleTitle: LogBase
second_title: .NET için Aspose.Words
description: Hassas veri görselleştirme ve gelişmiş grafik doğruluğu için AxisScaling LogBase özelliğinin logaritmik tabanını ayarlayın. Grafiklerinizi bugün optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

Logaritmik bir eksenin logaritmik tabanını alır veya ayarlar.

```csharp
public double LogBase { get; set; }
```

## Notlar

Özellik MS Office 2016 yeni grafikleri tarafından desteklenmiyor.

Kayan nokta değerinin geçerli aralığı 2'den büyük veya ona eşit ve 1000'den küçük veya ona eşittir. Özelliğin etkisi yalnızca şu durumlarda vardır:[`Type`](../type/) olarak ayarlandıLogarithmic.

Bu özelliğin ayarlanması,[`Type`](../type/) mülkLogarithmic .

## Örnekler

Bir grafik eksenine logaritmik ölçeklemenin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// Beş nokta için X/Y koordinatlı bir seri ekle.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// X ekseninin ölçeklenmesi varsayılan olarak doğrusaldır,
// X-değer aralığımızı (0, 1, 2, 3...) kapsayan eşit olarak artan değerleri görüntüleme.
// Y değerlerimiz için doğrusal bir eksen ideal değildir
// çünkü Y değeri daha küçük olan noktaların okunması daha zor olacaktır.
// 20 tabanlı logaritmik ölçekleme (1, 20, 400, 8000...)
// çizilen noktaları yayarak, grafikteki değerlerini daha kolay okumamızı sağlayacaktır.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Ayrıca bakınız

* class [AxisScaling](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
