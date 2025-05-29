---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: .NET için Aspose.Words
description: Aspose.Words.Drawing.Charts.Chart sınıfıyla güçlü grafik şekli özelliklerinin kilidini açın. Belgelerinizi dinamik görsel veri gösterimiyle geliştirin.
type: docs
weight: 880
url: /tr/net/aspose.words.drawing.charts/chart/
---
## Chart class

Grafik şekli özelliklerine erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class Chart
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Bu grafiğin tüm eksenlerinin bir koleksiyonunu alır. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Grafiğin birincil X ekseninin özelliklerine erişim sağlar. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Grafiğin birincil Y ekseninin özelliklerine erişim sağlar. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Grafiğin Z ekseninin özelliklerine erişim sağlar. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | Bu grafiğin veri tablosunun özelliklerine erişim sağlar. Veri tablosu, kullanılarak gösterilebilir.[`Show`](../chartdatatable/show/) mülk. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | Grafiğin dolgu ve satır biçimlendirmesine erişim sağlar. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Grafik efsanesi özelliklerine erişim sağlar. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Seri koleksiyonuna erişim sağlar. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | Bu grafiğin bir seri grubu koleksiyonuna erişim sağlar. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Bu grafiğin bağlı olduğu xls/xlsx dosyasının yolunu ve adını alır. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | Grafiğin stilini alır veya ayarlar. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Grafik başlığı özelliklerine erişim sağlar. |

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
