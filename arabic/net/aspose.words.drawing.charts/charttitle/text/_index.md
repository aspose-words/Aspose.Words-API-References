---
title: ChartTitle.Text
second_title: Aspose.Words لمراجع .NET API
description: ChartTitle ملكية. الحصول على نص عنوان المخطط أو تعيينه. Ifباطل أو تم تحديد قيمة فارغة سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

الحصول على نص عنوان المخطط أو تعيينه. If`باطل` أو تم تحديد قيمة فارغة، سيتم عرض العنوان الذي تم إنشاؤه تلقائيًا.

```csharp
public string Text { get; set; }
```

### ملاحظات

يستخدم[`Show`](../show/) الخيار إذا كنت بحاجة إلى إخفاء العنوان.

### أمثلة

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

* class [ChartTitle](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../charttitle/)
* المجسم [Aspose.Words](../../../)


