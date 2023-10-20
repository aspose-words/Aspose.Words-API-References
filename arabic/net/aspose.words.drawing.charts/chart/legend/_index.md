---
title: Chart.Legend
linktitle: Legend
articleTitle: Legend
second_title: Aspose.Words لـ .NET
description: Chart Legend ملكية. يوفر الوصول إلى خصائص وسيلة إيضاح المخطط في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

يوفر الوصول إلى خصائص وسيلة إيضاح المخطط.

```csharp
public ChartLegend Legend { get; }
```

## أمثلة

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
