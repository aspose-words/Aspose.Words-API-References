---
title: Chart
second_title: Aspose.Words for .NET API Referansı
description: Grafik şekli özelliklerine erişim sağlar.
type: docs
weight: 600
url: /tr/net/aspose.words.drawing.charts/chart/
---
## Chart class

Grafik şekli özelliklerine erişim sağlar.

```csharp
public class Chart
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx) { get; } | Grafiğin X ekseninin özelliklerine erişim sağlar. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy) { get; } | Grafiğin Y ekseninin özelliklerine erişim sağlar. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz) { get; } | Grafiğin Z ekseninin özelliklerine erişim sağlar. |
| [Legend](../../aspose.words.drawing.charts/chart/legend) { get; } | Grafik gösterge özelliklerine erişim sağlar. |
| [Series](../../aspose.words.drawing.charts/chart/series) { get; } | Seri koleksiyonuna erişim sağlar. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname) { get; set; } | Bu grafiğin bağlantılı olduğu bir xls/xlsx dosyasının yolunu ve adını alır. |
| [Title](../../aspose.words.drawing.charts/chart/title) { get; } | Grafik başlığı özelliklerine erişim sağlar. |

### Örnekler

Bir grafiğin nasıl ekleneceğini ve bir başlığın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belge oluşturucu ile bir grafik şekli ekleyin ve grafiğini alın.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Grafiğimize, grafik alanının üst ortasında görünen bir başlık vermek için "Başlık" özelliğini kullanın.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Başlığı görünür kılmak için "Show" özelliğini "true" olarak ayarlayın.
title.Show = true;

// "Kaplama" özelliğini "true" olarak ayarlayın Diğer grafik öğelerine, başlıkla çakışmalarına izin vererek daha fazla yer verin
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
