---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words لـ .NET
description: Chart Title ملكية. يوفر الوصول إلى خصائص عنوان المخطط في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

يوفر الوصول إلى خصائص عنوان المخطط.

```csharp
public ChartTitle Title { get; }
```

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
