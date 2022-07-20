---
title: Show
second_title: Aspose.Words لمراجع .NET API
description: لتحديد ما إذا كان العنوان سيظهر لهذا المخطط. القيمة الافتراضية هي صحيحة ._ x000d_
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

لتحديد ما إذا كان العنوان سيظهر لهذا المخطط. القيمة الافتراضية هي صحيحة ._ x000d_

```csharp
public bool Show { get; set; }
```

### أمثلة

يوضح كيفية إدراج مخطط وتعيين عنوان.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل شكل مخطط باستخدام أداة إنشاء المستندات واحصل على مخططها.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// استخدم خاصية "Title" لمنح المخطط عنوانًا يظهر في أعلى منتصف منطقة المخطط.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // اضبط خاصية "Show" على "true" لجعل العنوان مرئيًا.
title.Show = true;

// عيّن خاصية "التراكب" على "صواب" امنح عناصر المخطط الأخرى مساحة أكبر من خلال السماح لهم بتداخل العنوان
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### أنظر أيضا

* class [ChartTitle](../../charttitle)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../charttitle)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->