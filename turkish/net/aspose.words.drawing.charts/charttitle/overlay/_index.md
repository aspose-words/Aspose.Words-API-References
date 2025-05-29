---
title: ChartTitle.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: .NET için Aspose.Words
description: ChartTitle Overlay özelliğini keşfedin, daha net görseller için kontrol öğesi örtüşmesini sağlayın. Bu basit ayarla grafiklerinizi zahmetsizce geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/charttitle/overlay/
---
## ChartTitle.Overlay property

Diğer grafik öğelerinin başlıkla örtüşmesine izin verilip verilmeyeceğini belirler. Varsayılan olarak kaplama`YANLIŞ` .

```csharp
public bool Overlay { get; set; }
```

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

* class [ChartTitle](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
