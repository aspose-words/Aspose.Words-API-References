---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartSeriesGroup، التي تعمل على تبسيط إدارة خصائص سلسلة المخططات لتحسين تصور البيانات وتحليلها.
type: docs
weight: 1090
url: /ar/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

يمثل خصائص مجموعة سلسلة الرسم البياني، أي خصائص سلسلة الرسم البياني من نفس النوع المرتبطة بنفس المحاور.

```csharp
public class ChartSeriesGroup
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | يحصل على مجموعة المحاور التي تنتمي إليها مجموعة السلسلة هذه أو يعينها. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | يوفر الوصول إلى خصائص المحور X لهذه المجموعة المتسلسلة. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | يوفر الوصول إلى خصائص المحور Y لهذه المجموعة المتسلسلة. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | يحصل على حجم الفقاعات أو يعينه كنسبة مئوية من حجمها الافتراضي. |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | يحصل على حجم ثقب مخطط الدونات الرئيسي أو يعينه كنسبة مئوية. |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | يحصل على الزاوية، بالدرجات، للشريحة الأولى من مخطط الفطيرة الرئيسي أو يعينها. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | يحصل على النسبة المئوية لعرض الفجوة بين عناصر الرسم البياني أو يعينها. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | يحصل على النسبة المئوية لمدى تداخل أشرطة أو أعمدة السلسلة أو يعينها. |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | يحصل على حجم القسم الثانوي للمخطط الدائري أو يعينه كنسبة مئوية. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | يحصل على مجموعة من السلاسل التي تنتمي إلى مجموعة السلاسل هذه. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | يحصل على نوع سلسلة المخططات المضمنة في هذه المجموعة. |

## ملاحظات

تحتوي المخططات المجمعة على مجموعات متعددة من سلاسل المخططات، مع مجموعة منفصلة لكل نوع من أنواع السلاسل.

يمكنك أيضًا إنشاء مجموعة سلسلة مخططات لتعيين محاور ثانوية لسلسلة مخططات واحدة أو أكثر.

لمعرفة المزيد، قم بزيارة[ العمل مع المخططات البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

## أمثلة

يوضح كيفية العمل مع المحور الثانوي للرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

//حذف السلسلة المولدة افتراضيًا.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// قم بإنشاء مجموعة سلاسل إضافية، أيضًا من نوع الخط.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// حدد استخدام المحاور الثانوية لمجموعة السلسلة الجديدة.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
//إخفاء المحور X الثانوي.
newSeriesGroup.AxisX.Hidden = true;
// قم بتحديد عنوان المحور Y الثانوي.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

//أضف سلسلة إلى مجموعة السلسلة الجديدة.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
