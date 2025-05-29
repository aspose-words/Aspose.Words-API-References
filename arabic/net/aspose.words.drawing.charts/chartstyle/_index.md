---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words لـ .NET
description: طبّق أنماط الرسوم البيانية المُعدّة مُسبقًا في Aspose.Words. حسّن العروض المرئية باستخدام ChartStyle enum لتنسيق مستندات احترافي.
type: docs
weight: 1130
url: /ar/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

يحدد الأنماط المحددة مسبقًا للرسم البياني.

```csharp
public enum ChartStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Normal | `0` | يمثل نمط الرسم البياني الافتراضي. |
| Muted | `1` | نمط بألوان هادئة. |
| Saturated | `2` | نمط بألوان أكثر تشبعًا. |
| Shaded | `3` | نمط يحتوي على نقاط بيانات مظللة. |
| Flat | `4` | نمط بنقاط بيانات مسطحة بدون تدرج. |
| Shadowed | `5` | نمط يحتوي على نقاط بيانات تحتوي على ظل. |
| Gradient | `6` | نمط مع تعبئة متدرجة لنقاط البيانات. |
| Original | `7` | نمط ذو مظهر أصلي للرسم البياني. |
| Transparent1 | `8` | نمط بنقاط بيانات شفافة. |
| Transparent2 | `9` | نمط بنقاط بيانات شفافة. |
| Outline | `10` | نمط يحتوي على نقاط بيانات ليس لها تعبئة، ولكن لها مخطط تفصيلي فقط. |
| OutlineBlack | `11` | نمط ذو خلفية مخطط سوداء، حيث لا تحتوي نقاط البيانات على تعبئة، ولكن فقط مخطط تفصيلي. |
| Black | `12` | نمط مع خلفية مخططة باللون الأسود. |
| Grey | `13` | نمط مع خلفية مخطط متدرجة باللون الرمادي. |
| Blue | `14` | نمط مع خلفية مخطط زرقاء. |
| ShadedPlot | `15` | نمط يتم فيه تظليل منطقة الرسم البياني. |

## أمثلة

يوضح كيفية تعيين نمط الرسم البياني والحصول عليه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مخطط بالنمط الأسود.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// احصل على مخطط للتحديث.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// الحصول على نمط الرسم البياني.
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
