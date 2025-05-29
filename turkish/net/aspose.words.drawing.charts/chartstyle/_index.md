---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: .NET için Aspose.Words
description: Aspose.Words'de önceden tanımlanmış grafik stilleri uygulayın. Profesyonel belge biçimlendirmesi için görselleri ChartStyle enum'uyla geliştirin.
type: docs
weight: 1130
url: /tr/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

Bir grafiğin önceden tanımlanmış stillerini belirtir.

```csharp
public enum ChartStyle
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Normal | `0` | Varsayılan grafik stilini temsil eder. |
| Muted | `1` | Sönük renklere sahip bir stil. |
| Saturated | `2` | Daha doygun renklere sahip bir stil. |
| Shaded | `3` | Gölgeli veri noktalarına sahip bir stil. |
| Flat | `4` | Gradyansız düz veri noktalarına sahip bir stil. |
| Shadowed | `5` | Gölgesi olan veri noktalarına sahip bir stil. |
| Gradient | `6` | Veri noktalarının degrade dolgulu bir stili. |
| Original | `7` | Bir grafiğin orijinal görünümüne sahip bir stil. |
| Transparent1 | `8` | Şeffaf veri noktalarına sahip bir stil. |
| Transparent2 | `9` | Şeffaf veri noktalarına sahip bir stil. |
| Outline | `10` | Veri noktalarının dolgusu olmayan, yalnızca ana hatları olan bir stil. |
| OutlineBlack | `11` | Veri noktalarının dolgusunun olmadığı, yalnızca bir anahattının bulunduğu, siyah grafik arka planına sahip bir stil. |
| Black | `12` | Siyah grafik arka planına sahip bir stil. |
| Grey | `13` | Gri degradeli grafik arka planına sahip bir stil. |
| Blue | `14` | Mavi grafik arka planına sahip bir stil. |
| ShadedPlot | `15` | Arsa alanının gölgelendirildiği bir stil. |

## Örnekler

Grafik stilinin nasıl ayarlanacağını ve alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Siyah stilde bir grafik ekle.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// Güncellenecek bir grafik alın.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// Grafik stilini al.
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
