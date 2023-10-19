---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words for .NET
description: Chart Title mülk. Grafik başlığı özelliklerine erişim sağlar C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

Grafik başlığı özelliklerine erişim sağlar.

```csharp
public ChartTitle Title { get; }
```

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
