---
title: ChartTitle.Show
second_title: Aspose.Words for .NET API Referansı
description: ChartTitle mülk. Bu grafikte başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değerdoğru .
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

Bu grafikte başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değer:`doğru` .

```csharp
public bool Show { get; set; }
```

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

* class [ChartTitle](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../charttitle/)
* toplantı [Aspose.Words](../../../)


