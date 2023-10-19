---
title: ChartTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: ChartTitle Text mülk. Grafik başlığının metnini alır veya ayarlar. Ifhükümsüz veya boş değer belirtilirse otomatik oluşturulan başlık gösterilecektir C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Grafik başlığının metnini alır veya ayarlar. If`hükümsüz` veya boş değer belirtilirse otomatik oluşturulan başlık gösterilecektir.

```csharp
public string Text { get; set; }
```

## Notlar

Kullanmak[`Show`](../show/) Başlığı gizlemeniz gerekiyorsa bu seçeneği kullanın.

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

* class [ChartTitle](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
