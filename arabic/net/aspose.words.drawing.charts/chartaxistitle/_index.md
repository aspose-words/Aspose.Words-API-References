---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.ChartAxisTitle فصل. يوفر الوصول إلى خصائص عنوان المحور في C#.
type: docs
weight: 650
url: /ar/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

يوفر الوصول إلى خصائص عنوان المحور.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartAxisTitle
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | يحدد ما إذا كان سيتم السماح لعناصر المخطط الأخرى بتداخل العنوان. القيمة الافتراضية هي`خطأ شنيع` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | تحديد ما إذا كان سيتم عرض العنوان للمحور أم لا. القيمة الافتراضية هي`خطأ شنيع` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | الحصول على نص عنوان المحور أو تعيينه. If`باطل` أو تم تحديد قيمة فارغة، سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا. |

## أمثلة

يوضح كيفية تعيين عنوان محور المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// حذف السلسلة الافتراضية التي تم إنشاؤها.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// تعيين عنوان المحور.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
