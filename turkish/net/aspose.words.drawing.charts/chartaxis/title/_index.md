---
title: ChartAxis.Title
linktitle: Title
articleTitle: Title
second_title: .NET için Aspose.Words
description: Eksen başlıklarına kolay erişim ve özelleştirme için ChartAxis Title özelliğini keşfedin, böylece verilerinizin görselleştirilmesini ve sunumunu geliştirin.
type: docs
weight: 250
url: /tr/net/aspose.words.drawing.charts/chartaxis/title/
---
## ChartAxis.Title property

Eksen başlığı özelliklerine erişim sağlar.

```csharp
public ChartAxisTitle Title { get; }
```

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

* class [ChartAxisTitle](../../chartaxistitle/)
* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
