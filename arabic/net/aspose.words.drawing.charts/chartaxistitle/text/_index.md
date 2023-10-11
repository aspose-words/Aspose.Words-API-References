---
title: ChartAxisTitle.Text
second_title: Aspose.Words لمراجع .NET API
description: ChartAxisTitle ملكية. الحصول على نص عنوان المحور أو تعيينه. Ifباطل أو تم تحديد قيمة فارغة سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

الحصول على نص عنوان المحور أو تعيينه. If`باطل` أو تم تحديد قيمة فارغة، سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا.

```csharp
public string Text { get; set; }
```

### ملاحظات

يستخدم[`Show`](../show/) الخيار إذا كنت بحاجة إلى إظهار العنوان.

### أمثلة

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

* class [ChartAxisTitle](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* المجسم [Aspose.Words](../../../)


