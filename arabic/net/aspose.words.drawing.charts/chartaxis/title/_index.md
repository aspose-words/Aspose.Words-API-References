---
title: ChartAxis.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية عنوان ChartAxis لسهولة الوصول إلى عناوين المحاور وتخصيصها، مما يعزز تصور البيانات وعرضها.
type: docs
weight: 250
url: /ar/net/aspose.words.drawing.charts/chartaxis/title/
---
## ChartAxis.Title property

يوفر الوصول إلى خصائص عنوان المحور.

```csharp
public ChartAxisTitle Title { get; }
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

* class [ChartAxisTitle](../../chartaxistitle/)
* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
