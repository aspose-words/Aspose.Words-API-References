---
title: ChartAxisTitle.Text
second_title: Aspose.Words for .NET API Referansı
description: ChartAxisTitle mülk. Eksen başlığının metnini alır veya ayarlar. Ifhükümsüz veya boş değer belirtilirse otomatik oluşturulan başlık gösterilecektir.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Eksen başlığının metnini alır veya ayarlar. If`hükümsüz` veya boş değer belirtilirse otomatik oluşturulan başlık gösterilecektir.

```csharp
public string Text { get; set; }
```

### Notlar

Kullanmak[`Show`](../show/) başlığı göstermeniz gerekiyorsa bu seçeneği kullanın.

### Örnekler

Grafik ekseni başlığının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Varsayılan olarak oluşturulan seriyi silin.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Eksen başlığını ayarlayın.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Ayrıca bakınız

* class [ChartAxisTitle](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* toplantı [Aspose.Words](../../../)


