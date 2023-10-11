---
title: IChartDataPoint.Explosion
second_title: Aspose.Words لمراجع .NET API
description: IChartDataPoint ملكية. يحدد مقدار نقل نقطة البيانات من مركز الدائرة. يمكن أن يكون سالبًا ويعني السالب أنه لم يتم تعيين الخاصية ولا ينبغي تطبيق أي انفجار. ينطبق فقط على المخططات الدائرية.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

يحدد مقدار نقل نقطة البيانات من مركز الدائرة. يمكن أن يكون سالبًا، ويعني السالب أنه لم يتم تعيين الخاصية ولا ينبغي تطبيق أي انفجار. ينطبق فقط على المخططات الدائرية.

```csharp
public int Explosion { get; set; }
```

### أمثلة

يوضح كيفية نقل شرائح المخطط الدائري بعيدًا عن المركز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// يمكن نقل "شرائح" المخطط الدائري بعيدًا عن المركز بمسافة عبر سمة الانفجار الخاصة بنقطة البيانات المعنية.
// أضف نقطة بيانات إلى الجزء الأول من المخطط الدائري وانقلها بعيدًا عن المركز بمقدار 10 نقاط.
// يقوم Aspose.Words بإنشاء نقاط البيانات تلقائيًا في حالة عدم وجودها.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// قم بإزاحة الجزء الثاني لمسافة أكبر.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### أنظر أيضا

* interface [IChartDataPoint](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* المجسم [Aspose.Words](../../../)


