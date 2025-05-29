---
title: ChartTitle.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words لـ .NET
description: استكشف خاصية تنسيق ChartTitle لتحسين التعبئة وتصميم الخطوط، مما يمنح مخططاتك مظهرًا احترافيًا وأنيقًا.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/charttitle/format/
---
## ChartTitle.Format property

يوفر إمكانية الوصول إلى تنسيق التعبئة والخط لعنوان الرسم البياني.

```csharp
public ChartFormat Format { get; }
```

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

* class [ChartFormat](../../chartformat/)
* class [ChartTitle](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
