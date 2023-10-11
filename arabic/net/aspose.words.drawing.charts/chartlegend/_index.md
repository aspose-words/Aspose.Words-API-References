---
title: Class ChartLegend
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.ChartLegend فصل. يمثل خصائص وسيلة إيضاح المخطط.
type: docs
weight: 720
url: /ar/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

يمثل خصائص وسيلة إيضاح المخطط.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartLegend
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | إرجاع مجموعة من إدخالات وسيلة الإيضاح لجميع السلاسل وخطوط الاتجاه للمخطط الأصلي. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | يحدد ما إذا كان سيتم السماح لعناصر المخطط الأخرى بتداخل وسيلة الإيضاح أم لا. القيمة الافتراضية هي`خطأ شنيع` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | يحدد موضع وسيلة الإيضاح على المخطط. القيمة الافتراضية هيRight . |

### أمثلة

يوضح كيفية تحرير مظهر وسيلة إيضاح المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// انقل وسيلة إيضاح المخطط إلى الزاوية اليمنى العليا.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// امنح عناصر المخطط الأخرى، مثل الرسم البياني، مساحة أكبر من خلال السماح لها بتداخل وسيلة الإيضاح.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


