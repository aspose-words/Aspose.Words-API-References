---
title: ChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "انفجار نقاط بيانات المخطط" لضبط نقاط بيانات المخطط الدائري. تحكم في الحركة من المركز للحصول على تصورات مؤثرة. حسّن مخططاتك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartdatapoint/explosion/
---
## ChartDataPoint.Explosion property

يحدد مقدار نقل نقطة البيانات من مركز الفطيرة. يمكن أن يكون سلبيًا، ويعني السلبي أن الخاصية غير مضبوطة ولا ينبغي تطبيق أي انفجار. ينطبق فقط على المخططات الدائرية.

```csharp
public int Explosion { get; set; }
```

## أمثلة

يوضح كيفية نقل شرائح الرسم البياني الدائري بعيدًا عن المركز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// من الممكن نقل "شرائح" مخطط دائري بعيدًا عن المركز بمسافة عبر سمة الانفجار الخاصة بنقطة البيانات المعنية.
// أضف نقطة بيانات إلى الجزء الأول من مخطط الفطيرة وحركها بعيدًا عن المركز بـ 10 نقاط.
// يقوم Aspose.Words بإنشاء نقاط البيانات تلقائيًا إذا لم تكن موجودة.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

//إزاحة الجزء الثاني بمسافة أكبر.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### أنظر أيضا

* class [ChartDataPoint](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
