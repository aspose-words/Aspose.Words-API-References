---
title: Chart.Format
linktitle: Format
articleTitle: Format
second_title: .NET için Aspose.Words
description: Aracımızla gelişmiş grafik biçimlendirmenin kilidini açın! Veri sunumunuzu geliştiren çarpıcı, profesyonel görseller için dolgu ve çizgi stillerini kolayca özelleştirin.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing.charts/chart/format/
---
## Chart.Format property

Grafiğin dolgu ve satır biçimlendirmesine erişim sağlar.

```csharp
public ChartFormat Format { get; }
```

## Örnekler

Grafik biçimlendirmenin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Varsayılan olarak oluşturulan seriyi sil.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Grafik arka planını biçimlendir.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Eksen işareti etiketlerini gizle.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Grafik başlığını biçimlendir.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Eksen başlığını biçimlendir.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Efsaneyi biçimlendir.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Ayrıca bakınız

* class [ChartFormat](../../chartformat/)
* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
