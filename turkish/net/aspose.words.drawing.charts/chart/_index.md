---
title: Class Chart
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.Chart sınıf. Grafik şekli özelliklerine erişim sağlar.
type: docs
weight: 620
url: /tr/net/aspose.words.drawing.charts/chart/
---
## Chart class

Grafik şekli özelliklerine erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class Chart
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Bu grafiğin tüm eksenlerinin bir koleksiyonunu alır. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Grafiğin X ekseninin özelliklerine erişim sağlar. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Grafiğin Y ekseninin özelliklerine erişim sağlar. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Grafiğin Z ekseninin özelliklerine erişim sağlar. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Grafik açıklama özelliklerine erişim sağlar. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Seri koleksiyonuna erişim sağlar. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Bu grafiğin bağlı olduğu xls/xlsx dosyasının yolunu ve adını alır. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Grafik başlığı özelliklerine erişim sağlar. |

### Örnekler

Grafiğin nasıl ekleneceğini ve başlığın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belge oluşturucuyla bir grafik şekli ekleyin ve grafiğini alın.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Grafiğimize, grafik alanının üst orta kısmında görünen bir başlık vermek için "Başlık" özelliğini kullanın.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Başlığın görünür olması için "Show" özelliğini "true" olarak ayarlayın.
title.Show = true;

// "Overlay" özelliğini "true" olarak ayarlayın Diğer grafik öğelerinin başlıkla örtüşmesine izin vererek daha fazla alan sağlayın
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)


