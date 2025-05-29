---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: .NET için Aspose.Words
description: Eksen başlığı özelliklerini kolayca yönetmek ve belgenizin görsel etkisini artırmak için Aspose.Words.ChartAxisTitle sınıfını keşfedin.
type: docs
weight: 910
url: /tr/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Eksen başlığı özelliklerine erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[ Grafikleriyle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartAxisTitle
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | Eksen başlığının yazı tipi biçimlendirmesine erişim sağlar. |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | Eksen başlığının dolgu ve satır biçimlendirmesine erişim sağlar. |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Diğer grafik öğelerinin başlığın üzerine gelmesine izin verilip verilmeyeceğini belirler. Varsayılan değer`YANLIŞ` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Eksen için başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değer`YANLIŞ` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Eksen başlığının metnini alır veya ayarlar. Eğer`hükümsüz` veya boş değer belirtilirse, otomatik olarak oluşturulan başlık gösterilecektir. |

## Örnekler

Grafik eksen başlığının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Varsayılan olarak oluşturulan seriyi sil.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
