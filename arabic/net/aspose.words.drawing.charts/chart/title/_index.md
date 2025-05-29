---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية عنوان المخطط لسهولة التخصيص وتحسين الصور. أطلق العنان لإمكانات مخططاتك مع ميزات سهلة الاستخدام!
type: docs
weight: 120
url: /ar/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

يوفر الوصول إلى خصائص عنوان الرسم البياني.

```csharp
public ChartTitle Title { get; }
```

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
