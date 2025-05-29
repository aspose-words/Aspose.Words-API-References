---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için grafik başlıklarınızı kolayca yönetmek ve özelleştirmek amacıyla Aspose.Words.Drawing.Charts.ChartTitle sınıfını keşfedin.
type: docs
weight: 1140
url: /tr/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Grafik başlığı özelliklerine erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[ Grafikleriyle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartTitle
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | Grafik başlığının yazı tipi biçimlendirmesine erişim sağlar. |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | Grafik başlığının dolgu ve satır biçimlendirmesine erişim sağlar. |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Diğer grafik öğelerinin başlıkla örtüşmesine izin verilip verilmeyeceğini belirler. Varsayılan olarak kaplama`YANLIŞ` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Bu grafik için başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değer`doğru` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Grafik başlığının metnini alır veya ayarlar. Eğer`hükümsüz` veya boş değer belirtilirse, otomatik olarak oluşturulan başlık gösterilecektir. |

## Örnekler

Bir grafiğin nasıl ekleneceğini ve başlığın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir belge oluşturucu ile bir grafik şekli ekleyin ve grafiğini alın.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Grafiğimize, grafik alanının üst orta kısmında görünecek bir başlık vermek için "Başlık" özelliğini kullanın.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

 // Başlığı görünür kılmak için "Göster" özelliğini "true" olarak ayarlayın.
title.Show = true;

// "Üst Katman" özelliğini "doğru" olarak ayarlayın. Diğer grafik öğelerine, başlığın üzerine gelmelerine izin vererek daha fazla alan verin
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
