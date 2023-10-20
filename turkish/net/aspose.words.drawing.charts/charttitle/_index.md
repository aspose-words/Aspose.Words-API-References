---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartTitle sınıf. Grafik başlığı özelliklerine erişim sağlar C#'da.
type: docs
weight: 820
url: /tr/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Grafik başlığı özelliklerine erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[ Grafikleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartTitle
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Diğer grafik öğelerinin başlıkla örtüşmesine izin verilip verilmeyeceğini belirler. Varsayılan olarak yer paylaşımı`YANLIŞ` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Bu grafikte başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değer:`doğru` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Grafik başlığının metnini alır veya ayarlar. If`hükümsüz` veya boş değer belirtilirse otomatik oluşturulan başlık gösterilecektir. |

## Örnekler

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
