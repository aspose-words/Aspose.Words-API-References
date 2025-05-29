---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: .NET için Aspose.Words
description: Tasarımınızın görsel çekiciliğini ve tekdüzeliğini zahmetsizce artırarak tutarlı bir renk dolgusu elde etmek için Fill Solid yöntemini keşfedin.
type: docs
weight: 260
url: /tr/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Dolguyu tekdüze bir renge ayarlar.

```csharp
public void Solid()
```

## Notlar

Dolgulardan herhangi birini katı dolguya geri dönüştürmek için bu yöntemi kullanın.

## Örnekler

Herhangi bir dolgunun nasıl tekrar katı dolguya dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// İlk Çalıştırmanın Fontu için Fill nesnesini al.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Fontun Fill özelliklerini kontrol et.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Dolgu tipini düz yeşil renkte olacak şekilde değiştiriyoruz.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Ayrıca bakınız

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Dolguyu belirtilen tekdüze bir renge ayarlar.

```csharp
public void Solid(Color color)
```

## Notlar

Dolgulardan herhangi birini katı dolguya geri dönüştürmek için bu yöntemi kullanın.

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

* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
