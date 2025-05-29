---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.ShapeTextOrientation للتحكم بسهولة في اتجاه النص في الأشكال، مما يعزز تصميم مستندك وقابليته للقراءة.
type: docs
weight: 1680
url: /ar/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

يحدد اتجاه النص في الأشكال.

```csharp
public enum ShapeTextOrientation
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Horizontal | `0` | تم ترتيب النص أفقيًا (lr-tb). |
| Downward | `1` | يتم تدوير النص بمقدار 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl). |
| Upward | `2` | يتم تدوير النص بمقدار 90 درجة إلى اليسار ليظهر من الأسفل إلى الأعلى (bt-lr). |
| VerticalFarEast | `3` | تظهر أحرف الشرق الأقصى بشكل عمودي، ويتم تدوير النص الآخر بمقدار 90 درجة إلى اليمين لتظهر من أعلى إلى أسفل (tb-rl-v). |
| VerticalRotatedFarEast | `4` | تظهر أحرف الشرق الأقصى بشكل عمودي، ويتم تدوير النص الآخر بمقدار 90 درجة إلى اليمين لتظهر من أعلى إلى أسفل عموديًا، ثم من اليسار إلى اليمين أفقيًا (tb-lr-v). |
| WordArtVertical | `5` | النص عمودي، حيث يكون الحرف فوق الآخر. |
| WordArtVerticalRightToLeft | `6` | النص عمودي، مع وضع حرف واحد فوق الآخر، ثم من اليمين إلى اليسار أفقيًا. |

## أمثلة

يوضح كيفية تغيير الاتجاه والدوران لملصقات البيانات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

//إظهار تسميات البيانات.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// قم بتحديد شكل تسمية البيانات.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// تعيين اتجاه تسمية البيانات وتدويرها للسلسلة بأكملها.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// تغيير الاتجاه والدوران لعلامة البيانات الأولى.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
