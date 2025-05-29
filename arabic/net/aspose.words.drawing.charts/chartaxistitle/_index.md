---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.ChartAxisTitle لإدارة خصائص عنوان المحور بسهولة وتعزيز التأثير البصري للمستند الخاص بك.
type: docs
weight: 910
url: /ar/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

يوفر الوصول إلى خصائص عنوان المحور.

لمعرفة المزيد، قم بزيارة[العمل مع المخططات](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartAxisTitle
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | يوفر الوصول إلى تنسيق الخط لعنوان المحور. |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | يوفر إمكانية الوصول إلى تنسيق التعبئة والخطوط لعنوان المحور. |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | يحدد ما إذا كان سيتم السماح لعناصر الرسم البياني الأخرى بالتداخل مع العنوان. القيمة الافتراضية هي`خطأ شنيع` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | يحدد ما إذا كان سيتم عرض العنوان للمحور. القيمة الافتراضية هي`خطأ شنيع` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | يحصل على نص عنوان المحور أو يعينه. إذا`باطل` أو إذا تم تحديد قيمة فارغة، سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا. |

## أمثلة

يوضح كيفية تعيين عنوان محور الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
//حذف السلسلة المولدة افتراضيًا.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
