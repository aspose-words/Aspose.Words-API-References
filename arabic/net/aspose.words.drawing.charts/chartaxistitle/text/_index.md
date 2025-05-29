---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية نص عنوان محور الرسم البياني لتخصيص عناوين محاورك بسهولة. عيّن أو احصل على عناوين ديناميكية لتحسين عرض البيانات.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

يحصل على نص عنوان المحور أو يعينه. إذا`باطل` أو إذا تم تحديد قيمة فارغة، سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا.

```csharp
public string Text { get; set; }
```

## ملاحظات

يستخدم[`Show`](../show/)الخيار إذا كنت بحاجة إلى إظهار العنوان.

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

* class [ChartAxisTitle](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
