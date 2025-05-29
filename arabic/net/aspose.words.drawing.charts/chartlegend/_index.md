---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartLegend لتحسين مخططاتك باستخدام خصائص الأسطورة القابلة للتخصيص لتحسين تصور البيانات.
type: docs
weight: 1010
url: /ar/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

يمثل خصائص أسطورة الرسم البياني.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartLegend
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegend/font/) { get; } | يتيح الوصول إلى تنسيق الخط الافتراضي لإدخالات التسمية التوضيحية. لتجاوز تنسيق الخط لـ إدخال تسمية توضيحية محدد، استخدم[`Font`](../chartlegendentry/font/) الملكية. |
| [Format](../../aspose.words.drawing.charts/chartlegend/format/) { get; } | يوفر إمكانية الوصول إلى تعبئة وتنسيق السطر الخاص بالأسطورة. |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | يقوم بإرجاع مجموعة من إدخالات الأسطورة لجميع السلاسل وخطوط الاتجاه للرسم البياني الرئيسي. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | يحدد ما إذا كان سيتم السماح لعناصر الرسم البياني الأخرى بالتداخل مع الأسطورة. القيمة الافتراضية هي`خطأ شنيع` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | يحدد موضع الأسطورة على الرسم البياني. |

## أمثلة

يوضح كيفية تحرير مظهر أسطورة الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// نقل أسطورة الرسم البياني إلى الزاوية اليمنى العليا.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// امنح عناصر الرسم البياني الأخرى، مثل الرسم البياني، مساحة أكبر من خلال السماح لها بالتداخل مع الأسطورة.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
