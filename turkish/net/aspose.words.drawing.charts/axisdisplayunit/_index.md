---
title: AxisDisplayUnit Class
linktitle: AxisDisplayUnit
articleTitle: AxisDisplayUnit
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.AxisDisplayUnit sınıf. Değer ekseni için görüntüleme birimlerinin ölçeklendirme seçeneklerine erişim sağlar C#'da.
type: docs
weight: 550
url: /tr/net/aspose.words.drawing.charts/axisdisplayunit/
---
## AxisDisplayUnit class

Değer ekseni için görüntüleme birimlerinin ölçeklendirme seçeneklerine erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class AxisDisplayUnit
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [AxisDisplayUnit](axisdisplayunit/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomUnit](../../aspose.words.drawing.charts/axisdisplayunit/customunit/) { get; set; } | Görüntü birimlerini değer ekseninde ölçeklendirmek için kullanıcı tanımlı bir bölen alır veya ayarlar. |
| [Document](../../aspose.words.drawing.charts/axisdisplayunit/document/) { get; } | Tapu sahibinin ait olduğu Belgeyi döndürür. |
| [Unit](../../aspose.words.drawing.charts/axisdisplayunit/unit/) { get; set; } | Görüntü birimlerinin ölçeklendirme değerini önceden tanımlanmış değerlerden biri olarak alır veya ayarlar. |

## Örnekler

Bir grafik ekseninin onay işaretlerinin ve görüntülenen değerlerinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Y ekseninin küçük onay işaretlerini çizim alanından uzağa bakacak şekilde ayarlayın,
// ve ekseni geçmek için ana onay işaretleri.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Y eksenini her 10 birimde bir büyük işaret ve her 1 birimde bir küçük işaret gösterecek şekilde ayarlayın.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Y ekseni sınırlarını -10 ve 20 olarak ayarlayın.
// Bu Y ekseni artık 4 ana onay işareti ve 27 küçük onay işareti görüntüleyecek.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// X ekseni için her 10 birimde ana onay işaretlerini ayarlayın,
// 2,5 birimdeki her küçük onay işareti.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Her iki onay işareti türünü de grafik çizim alanında görünecek şekilde yapılandırın.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// X ekseni sınırlarını, X ekseni 5 ana onay işaretini ve 12 ikincil onay işaretini kapsayacak şekilde ayarlayın.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Onay etiketlerini değerlerini milyon cinsinden gösterecek şekilde ayarlayın.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Onay etiketlerinin değerlerini göstereceği daha spesifik bir değer ayarlayabiliriz.
// Bu ifade yukarıdakine eşdeğerdir.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
