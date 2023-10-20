---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.ChartTitle فصل. يوفر الوصول إلى خصائص عنوان المخطط في C#.
type: docs
weight: 820
url: /ar/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

يوفر الوصول إلى خصائص عنوان المخطط.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartTitle
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | يحدد ما إذا كان سيتم السماح لعناصر المخطط الأخرى بتداخل العنوان. بشكل افتراضي يكون التراكب`خطأ شنيع` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | يحدد ما إذا كان سيتم عرض العنوان لهذا المخطط أم لا. القيمة الافتراضية هي`حقيقي` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | الحصول على نص عنوان المخطط أو تعيينه. If`باطل` أو تم تحديد قيمة فارغة، سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا. |

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
