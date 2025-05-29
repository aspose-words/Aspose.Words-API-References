---
title: ChartTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words لـ .NET
description: حسّن مخططاتك بعناوين قابلة للتخصيص. تحكم بسهولة في الرؤية - الإعداد الافتراضي هو "صحيح". ارتقِ بعرض بياناتك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

يحدد ما إذا كان سيتم عرض العنوان لهذا الرسم البياني. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool Show { get; set; }
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

* class [ChartTitle](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
