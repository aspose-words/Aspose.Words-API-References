---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words لـ .NET
description: ChartLegend Position ملكية. يحدد موضع وسيلة الإيضاح على المخطط. القيمة الافتراضية هيRight  في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

يحدد موضع وسيلة الإيضاح على المخطط. القيمة الافتراضية هيRight .

```csharp
public LegendPosition Position { get; set; }
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

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
