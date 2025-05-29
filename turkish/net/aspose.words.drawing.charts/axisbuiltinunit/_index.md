---
title: AxisBuiltInUnit Enum
linktitle: AxisBuiltInUnit
articleTitle: AxisBuiltInUnit
second_title: .NET için Aspose.Words
description: Özelleştirilebilir eksen görüntüleme birimleri için Aspose.Words.Drawing.Charts.AxisBuiltInUnit enum'unu keşfedin, grafiğinizin netliğini ve etkinliğini artırın.
type: docs
weight: 760
url: /tr/net/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enumeration

Bir eksen için görüntüleme birimlerini belirtir.

```csharp
public enum AxisBuiltInUnit
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Grafikteki değerlerin olduğu gibi görüntülenmesini belirtir. |
| Custom | `1` | Grafikteki değerlerin kullanıcı tanımlı bir bölenle bölünmesini belirtir. Bu değer, MS Office 2016'nın yeni grafik türleri tarafından desteklenmez. |
| Billions | `2` | Grafikteki değerlerin 1.000.000.000'a bölünmesini belirtir. |
| HundredMillions | `3` | Grafikteki değerlerin 100.000.000'a bölünmesini belirtir. |
| Hundreds | `4` | Grafikteki değerlerin 100'e bölünmesini belirtir. |
| HundredThousands | `5` | Grafikteki değerlerin 100.000'e bölünmesini belirtir. |
| Millions | `6` | Grafikteki değerlerin 1.000.000'a bölünmesini belirtir. |
| TenMillions | `7` | Grafikteki değerlerin 10.000.000'a bölünmesini belirtir. |
| TenThousands | `8` | Grafikteki değerlerin 10.000'e bölünmesini belirtir. |
| Thousands | `9` | Grafikteki değerlerin 1.000'e bölünmesini belirtir. |
| Trillions | `10` | Grafikteki değerlerin 1.000.000.000.0000'a bölünmesini belirtir. |
| Percentage | `11` | Grafikteki değerlerin 0,01'e bölünmesini belirtir. Bu değer yalnızca MS Office 2016'nın yeni chart türleri tarafından desteklenir. |

## Örnekler

Bir grafik ekseninin işaretlerinin ve görüntülenen değerlerinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Y ekseninin küçük işaretlerini çizim alanından uzağa bakacak şekilde ayarlayın,
// ve ekseni geçmek için büyük işaretler.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Y eksenini her 10 birimde bir büyük bir işaret ve her 1 birimde bir küçük bir işaret gösterecek şekilde ayarlayın.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Y ekseninin sınırlarını -10 ve 20 olarak ayarlayın.
// Bu Y ekseni artık 4 ana işaret ve 27 küçük işaret gösterecek.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// X ekseni için, ana işaret noktalarını her 10 birimde bir ayarlayın,
// her küçük tik işareti 2,5 birimde.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Her iki tür işaretin de grafik çizim alanı içerisinde görünmesini yapılandırın.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// X ekseninin sınırlarını, X ekseninin 5 ana çizgi ve 12 küçük çizgiyi kapsayacak şekilde ayarlayın.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// Tik etiketlerini milyon cinsinden değerlerini gösterecek şekilde ayarlayın.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Tik etiketlerinin değerlerini hangi değere göre görüntüleyeceğini daha spesifik bir değere ayarlayabiliriz.
// Bu ifade yukarıdaki ifadeye eşdeğerdir.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
