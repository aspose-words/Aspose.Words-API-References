---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: .NET için Aspose.Words
description: Gelişmiş grafik öğesi stili için Aspose.Words.ChartFormat sınıfını keşfedin. Belgelerinizi profesyonel, özelleştirilebilir grafik tasarımlarıyla geliştirin.
type: docs
weight: 1000
url: /tr/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

Bir grafik öğesinin biçimlendirmesini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | Üst grafik öğesi için doldurma biçimlendirmesini alır. |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | Herhangi bir formatın tanımlanıp tanımlanmadığını belirten bir bayrak alır. |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | Üst grafik öğesinin şekil türünü alır veya ayarlar. |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | Üst grafik öğesi için satır biçimlendirmesini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | Grafik öğesinin dolgusunu varsayılan değere sahip olacak şekilde sıfırlar. |

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
