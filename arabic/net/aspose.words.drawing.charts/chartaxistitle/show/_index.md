---
title: ChartAxisTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "عرض عنوان محور الرسم البياني" للتحكم في رؤية عناوين المحاور. حسّن مخططاتك بعناوين واضحة وغنية بالمعلومات للحصول على رؤى أفضل للبيانات.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/chartaxistitle/show/
---
## ChartAxisTitle.Show property

يحدد ما إذا كان سيتم عرض العنوان للمحور. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool Show { get; set; }
```

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
