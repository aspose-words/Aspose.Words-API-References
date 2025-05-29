---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.PresetTexture لتعزيز أشكالك باستخدام مواد قابلة للتخصيص للحصول على تصميمات مستندات مذهلة.
type: docs
weight: 1560
url: /ar/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

يحدد الملمس الذي سيتم استخدامه لملء الشكل.

```csharp
public enum PresetTexture
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `-1` | لا يوجد نسيج. |
| BlueTissuePaper | `1` | نسيج ورقي أزرق. |
| Bouquet | `2` | نسيج الباقة. |
| BrownMarble | `3` | نسيج رخام بني. |
| Canvas | `4` | نسيج القماش. |
| Cork | `5` | نسيج الفلين. |
| Denim | `6` | نسيج الدنيم. |
| FishFossil | `7` | نسيج أحفوري للأسماك. |
| Granite | `8` | نسيج الجرانيت. |
| GreenMarble | `9` | نسيج الرخام الأخضر. |
| MediumWood | `10` | نسيج خشب متوسط. |
| Newsprint | `11` | نسيج ورق الصحف. |
| Oak | `12` | نسيج البلوط. |
| PaperBag | `13` | نسيج كيس ورقي. |
| Papyrus | `14` | نسيج البردي. |
| Parchment | `15` | نسيج الرق. |
| PinkTissuePaper | `16` | نسيج ورقي وردي. |
| PurpleMesh | `17` | نسيج شبكي أرجواني. |
| RecycledPaper | `18` | نسيج ورق معاد تدويره. |
| Sand | `19` | نسيج الرمل. |
| Stationery | `20` | نسيج القرطاسية. |
| Walnut | `21` | نسيج الجوز. |
| WaterDroplets | `22` | نسيج قطرات الماء. |
| WhiteMarble | `23` | نسيج الرخام الأبيض. |
| WovenMat | `24` | نسيج حصيرة منسوجة. |

## أمثلة

إظهار كيفية تعيين تنسيق العلامة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// تعيين تنسيق العلامة.
series.Marker.Size = 40;
series.Marker.Symbol = MarkerSymbol.Square;
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Marker.Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[0].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[0].Marker.Format.Stroke.BackColor = Color.Red;
dataPoints[1].Marker.Format.Fill.PresetTextured(PresetTexture.WaterDroplets);
dataPoints[1].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[1].Marker.Format.Stroke.Visible = false;
dataPoints[2].Marker.Format.Fill.PresetTextured(PresetTexture.GreenMarble);
dataPoints[2].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Fill.PresetTextured(PresetTexture.Oak);
dataPoints[3].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Stroke.Transparency = 0.5;

doc.Save(ArtifactsDir + "Charts.MarkerFormatting.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
