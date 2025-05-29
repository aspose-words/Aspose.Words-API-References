---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words لـ .NET
description: استخدم خصائص أشكال المخططات البيانية الفعّالة مع فئة Aspose.Words.Drawing.Charts.Chart. حسّن مستنداتك بتمثيل بيانات بصري ديناميكي.
type: docs
weight: 880
url: /ar/net/aspose.words.drawing.charts/chart/
---
## Chart class

يوفر الوصول إلى خصائص شكل الرسم البياني.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class Chart
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | يحصل على مجموعة من جميع محاور هذا الرسم البياني. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | يوفر الوصول إلى خصائص المحور X الأساسي للرسم البياني. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | يوفر الوصول إلى خصائص المحور Y الأساسي للرسم البياني. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | يوفر الوصول إلى خصائص المحور Z للرسم البياني. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | يوفر الوصول إلى خصائص جدول البيانات لهذا الرسم البياني. يمكن عرض جدول البيانات باستخدام[`Show`](../chartdatatable/show/) الملكية. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | يوفر إمكانية الوصول إلى تعبئة وتنسيق الخطوط للرسم البياني. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | يوفر الوصول إلى خصائص أسطورة الرسم البياني. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | يوفر الوصول إلى مجموعة السلسلة. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | يوفر الوصول إلى مجموعة تسلسلية من هذا الرسم البياني. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | يحصل على المسار واسم ملف xls/xlsx الذي يرتبط به هذا الرسم البياني. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | يحصل على نمط الرسم البياني أو يعينه. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | يوفر الوصول إلى خصائص عنوان الرسم البياني. |

## أمثلة

يوضح كيفية إدراج مخطط وتعيين عنوان.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج شكل مخطط باستخدام منشئ المستندات واحصل على مخططه.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

//استخدم خاصية "العنوان" لإعطاء عنوان لمخططنا، والذي يظهر في الجزء العلوي الأوسط من منطقة المخطط.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

 // قم بضبط خاصية "إظهار" على "صحيح" لجعل العنوان مرئيًا.
title.Show = true;

// اضبط خاصية "Overlay" على "true" امنح عناصر الرسم البياني الأخرى مساحة أكبر من خلال السماح لها بالتداخل مع العنوان
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
