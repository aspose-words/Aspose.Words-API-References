---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.ChartFormat لتصميم عناصر المخططات البيانية بشكل متقدم. حسّن مستنداتك بتصميمات مخططات بيانية احترافية وقابلة للتخصيص.
type: docs
weight: 1000
url: /ar/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

يمثل تنسيق عنصر الرسم البياني.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | يحصل على تنسيق التعبئة لعنصر الرسم البياني الرئيسي. |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | يحصل على علم يشير إلى ما إذا كان قد تم تعريف أي تنسيق. |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | يحصل على نوع الشكل لعنصر الرسم البياني الرئيسي أو يعينه. |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | يحصل على تنسيق السطر لعنصر الرسم البياني الرئيسي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | إعادة تعيين تعبئة عنصر الرسم البياني للحصول على القيمة الافتراضية. |

## أمثلة

يوضح كيفية استخدام تنسيق الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

//حذف السلسلة التي تم إنشاؤها افتراضيًا.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

//تنسيق خلفية الرسم البياني.
chart.Format.Fill.Solid(Color.DarkSlateGray);

//إخفاء علامات المحور.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

//تنسيق عنوان الرسم البياني.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

//تنسيق عنوان المحور.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

//تنسيق الأسطورة.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
