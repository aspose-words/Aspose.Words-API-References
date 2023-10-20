---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.Chart فصل. يوفر الوصول إلى خصائص شكل المخطط في C#.
type: docs
weight: 620
url: /ar/net/aspose.words.drawing.charts/chart/
---
## Chart class

يوفر الوصول إلى خصائص شكل المخطط.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class Chart
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | الحصول على مجموعة من جميع محاور هذا المخطط. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | يوفر الوصول إلى خصائص المحور X للمخطط. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | يوفر الوصول إلى خصائص المحور Y للمخطط. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | يوفر الوصول إلى خصائص المحور Z للمخطط. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | يوفر الوصول إلى خصائص وسيلة إيضاح المخطط. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | يوفر الوصول إلى مجموعة السلسلة. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | يحصل على مسار واسم ملف xls/xlsx الذي يرتبط به هذا المخطط. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | يوفر الوصول إلى خصائص عنوان المخطط. |

## أمثلة

يوضح كيفية إدراج مخطط وتعيين عنوان.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج شكل مخطط باستخدام أداة إنشاء المستندات واحصل على مخططه.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// استخدم خاصية "العنوان" لإعطاء مخططنا عنوانًا، والذي يظهر في الجزء العلوي الأوسط من منطقة المخطط.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // اضبط خاصية "إظهار" على "صحيح" لجعل العنوان مرئيًا.
title.Show = true;

// اضبط خاصية "التراكب" على "صحيح" امنح عناصر المخطط الأخرى مساحة أكبر من خلال السماح لها بتداخل العنوان
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
